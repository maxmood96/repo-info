<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `julia`

-	[`julia:1`](#julia1)
-	[`julia:1-alpine`](#julia1-alpine)
-	[`julia:1-alpine3.18`](#julia1-alpine318)
-	[`julia:1-alpine3.19`](#julia1-alpine319)
-	[`julia:1-bookworm`](#julia1-bookworm)
-	[`julia:1-bullseye`](#julia1-bullseye)
-	[`julia:1-windowsservercore`](#julia1-windowsservercore)
-	[`julia:1-windowsservercore-1809`](#julia1-windowsservercore-1809)
-	[`julia:1-windowsservercore-ltsc2022`](#julia1-windowsservercore-ltsc2022)
-	[`julia:1.10`](#julia110)
-	[`julia:1.10-alpine`](#julia110-alpine)
-	[`julia:1.10-alpine3.18`](#julia110-alpine318)
-	[`julia:1.10-alpine3.19`](#julia110-alpine319)
-	[`julia:1.10-bookworm`](#julia110-bookworm)
-	[`julia:1.10-bullseye`](#julia110-bullseye)
-	[`julia:1.10-windowsservercore`](#julia110-windowsservercore)
-	[`julia:1.10-windowsservercore-1809`](#julia110-windowsservercore-1809)
-	[`julia:1.10-windowsservercore-ltsc2022`](#julia110-windowsservercore-ltsc2022)
-	[`julia:1.10.0`](#julia1100)
-	[`julia:1.10.0-alpine`](#julia1100-alpine)
-	[`julia:1.10.0-alpine3.18`](#julia1100-alpine318)
-	[`julia:1.10.0-alpine3.19`](#julia1100-alpine319)
-	[`julia:1.10.0-bookworm`](#julia1100-bookworm)
-	[`julia:1.10.0-bullseye`](#julia1100-bullseye)
-	[`julia:1.10.0-windowsservercore`](#julia1100-windowsservercore)
-	[`julia:1.10.0-windowsservercore-1809`](#julia1100-windowsservercore-1809)
-	[`julia:1.10.0-windowsservercore-ltsc2022`](#julia1100-windowsservercore-ltsc2022)
-	[`julia:1.6`](#julia16)
-	[`julia:1.6-alpine`](#julia16-alpine)
-	[`julia:1.6-alpine3.18`](#julia16-alpine318)
-	[`julia:1.6-alpine3.19`](#julia16-alpine319)
-	[`julia:1.6-bookworm`](#julia16-bookworm)
-	[`julia:1.6-bullseye`](#julia16-bullseye)
-	[`julia:1.6-windowsservercore`](#julia16-windowsservercore)
-	[`julia:1.6-windowsservercore-1809`](#julia16-windowsservercore-1809)
-	[`julia:1.6-windowsservercore-ltsc2022`](#julia16-windowsservercore-ltsc2022)
-	[`julia:1.6.7`](#julia167)
-	[`julia:1.6.7-alpine`](#julia167-alpine)
-	[`julia:1.6.7-alpine3.18`](#julia167-alpine318)
-	[`julia:1.6.7-alpine3.19`](#julia167-alpine319)
-	[`julia:1.6.7-bookworm`](#julia167-bookworm)
-	[`julia:1.6.7-bullseye`](#julia167-bullseye)
-	[`julia:1.6.7-windowsservercore`](#julia167-windowsservercore)
-	[`julia:1.6.7-windowsservercore-1809`](#julia167-windowsservercore-1809)
-	[`julia:1.6.7-windowsservercore-ltsc2022`](#julia167-windowsservercore-ltsc2022)
-	[`julia:alpine`](#juliaalpine)
-	[`julia:alpine3.18`](#juliaalpine318)
-	[`julia:alpine3.19`](#juliaalpine319)
-	[`julia:bookworm`](#juliabookworm)
-	[`julia:bullseye`](#juliabullseye)
-	[`julia:latest`](#julialatest)
-	[`julia:windowsservercore`](#juliawindowsservercore)
-	[`julia:windowsservercore-1809`](#juliawindowsservercore-1809)
-	[`julia:windowsservercore-ltsc2022`](#juliawindowsservercore-ltsc2022)

## `julia:1`

```console
$ docker pull julia@sha256:564460379e4782890dbfe5f073481eceb044b96cefb69f45805f9901fee5a747
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
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `julia:1` - linux; amd64

```console
$ docker pull julia@sha256:c581649ac221ebfbea9798a3bd66dfb0ba0dd44ba20ff5262d3c8bb93a759346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.9 MB (205909072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b184ca25c5acda81d0dc2e137ccf411bdd8e9f61fdd835d4bd55637d23b835`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad1c4eb009e797d65c1acfac69cd12c8f9060f29f760108f933027f2caab9c3`  
		Last Modified: Tue, 13 Feb 2024 01:53:54 GMT  
		Size: 5.7 MB (5707977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef8b6ee7f7fb149365afb062c086c37b5b314813fc6ec90095b002f5a925f0b`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 171.1 MB (171076635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d82177bdd251b5f04cc2ba1e5fd4efbafdbd4770a176a106cc21f400dbc05a`  
		Last Modified: Tue, 13 Feb 2024 01:53:54 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:3b5ca3771866b183000dca0a20d1bd2cb30d18b3a75d2ff32ac5cacaf423ef41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2158401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1bf8696406f25674e86fbc2d37065b3233c46aeb745f75fb02a0207775ca9a`

```dockerfile
```

-	Layers:
	-	`sha256:0884c94ffa8afd7175e4fdf92aa18f71815867215f0cde964240ba45b4f94154`  
		Last Modified: Tue, 13 Feb 2024 01:53:54 GMT  
		Size: 2.1 MB (2139045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:348b64f895c758148af65a9d8d6cf1581a93e955b08d7c118bee6923d2672bda`  
		Last Modified: Tue, 13 Feb 2024 01:53:54 GMT  
		Size: 19.4 KB (19356 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:c7b50eb125b7d60c63329a2c13798bc0c6e71611739c313a8ac466b505e9daab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199068374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc9cfd7eb49e87c970aa3df455f5951bd13608a351ad60fa41258f33c872dad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b14e605bd6638a1976eeb8d1cde59556a1f77295bac46d1669a9e27e6cd0ad6`  
		Last Modified: Wed, 14 Feb 2024 00:40:29 GMT  
		Size: 5.5 MB (5533149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d7d4913392d7182590a28188bd4fa882d0ed53f36bf9d49c1b5dfd74dda0ce`  
		Last Modified: Wed, 14 Feb 2024 00:40:32 GMT  
		Size: 164.4 MB (164378492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c05a2fc2483ea3c18ac5829c7ca9c7c9fd40204cb09b4ace74a3c02cb27dbe9`  
		Last Modified: Wed, 14 Feb 2024 00:40:28 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:7812cc45c880626d2dfa14638dfc0dcca6d09a54e1b49abf8d917a8f8a6fd61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2157622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d96f6d9b1c89aaf182d67e03efcae208a6f69ae643a004df4c24d36a84b881f`

```dockerfile
```

-	Layers:
	-	`sha256:ffca818dcaa241a02e65213ba00b90e138a6c248aaa839bb326ddf81d27472f1`  
		Last Modified: Wed, 14 Feb 2024 00:40:29 GMT  
		Size: 2.1 MB (2138415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7b32281e96ad074af12b3d2e1fec978b2b8afb5106ab0eeb89189cedc13c81d`  
		Last Modified: Wed, 14 Feb 2024 00:40:29 GMT  
		Size: 19.2 KB (19207 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - linux; 386

```console
$ docker pull julia@sha256:ed5dae7c246f3779da0892e59fefc8a2a06c1b0418c75cc66df890b64fbd5d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192476013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266a487238b5f50dc9dd3bc262639f4da7f6d7b6194a3f48742cf1725df03675`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adcfe329152d3631bed65ca802c4d591cf2466ececc127b4689e12fd044b6dd9`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 5.9 MB (5863232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7f556d75a67e2c4d02467097026cac3136c670701b05d1fe37c2209b150c66`  
		Last Modified: Tue, 13 Feb 2024 01:53:58 GMT  
		Size: 156.5 MB (156470603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee51a4a243b601cbdaea50eb3df43c6297660d3956259740ebcbb63126d2d0a`  
		Last Modified: Tue, 13 Feb 2024 01:53:54 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:98bc5d459492dc920f2634c7d2a39252f464f40045e8ee9bb9a967df561e7fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2155528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741936c96e550374e6be8d4320cd5b8e3cf1b315e382afac934f7edfc2236eb3`

```dockerfile
```

-	Layers:
	-	`sha256:53aa4312033ace4a7cf6f547e9085d8bd6890df5b2615d784fc182399ed92297`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 2.1 MB (2136223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3060f20bd073e1f89280df62e40daa82ac66677706d6628b0e7ce70250402b51`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 19.3 KB (19305 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - linux; ppc64le

```console
$ docker pull julia@sha256:42518fad4d8a20363e408d6bf3ce4259a1203bc1f3a1720ede05055daf233cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.3 MB (193349040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc361617127c03f5ef43a89da3fa93390c1213068a6e940b721330dc4e63a12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:b65bdf3d9277efbf6bbf8bf0121f92bdcd342ed0c4f49f1cee3b91adafacd76c in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b1cce6d9947985e4270ac998aa258401bc5deca94d504040a14f9f3c47258d68`  
		Last Modified: Tue, 13 Feb 2024 00:43:56 GMT  
		Size: 33.1 MB (33118908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a48b566372cb4fa0fec129e803c39a28de529b9736fd03a42344641249c1fc`  
		Last Modified: Tue, 13 Feb 2024 21:54:44 GMT  
		Size: 6.2 MB (6239799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85e6dfe440366f653bf664315e491fe0cb2bb189428018fbcf657460fbbc3fa`  
		Last Modified: Tue, 13 Feb 2024 21:54:47 GMT  
		Size: 154.0 MB (153989961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6306b805ea4661e164d23cfd0d8dfae9d27c498477a790d3351d0f6ecc3e5fd`  
		Last Modified: Tue, 13 Feb 2024 21:54:43 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:8ed461f46641215c54d31c67c06954851c85f63b1d2b4eebe9351ecff9289da9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2161862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286b8e56e5b1f465b474b30b2fe8512b0c2238bef520a8bd95c4e5e31b59df2c`

```dockerfile
```

-	Layers:
	-	`sha256:9da0b3fffb06b598b8c17e331a4e70d4e6b54c5bfad5a40d4e88a16d3966ab41`  
		Last Modified: Tue, 13 Feb 2024 21:54:43 GMT  
		Size: 2.1 MB (2142609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbfe360df232fd616240d3f8aae495b7a956d6a7383dcdf4dc8ae56cd7d319c2`  
		Last Modified: Tue, 13 Feb 2024 21:54:43 GMT  
		Size: 19.3 KB (19253 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - windows version 10.0.20348.2227; amd64

```console
$ docker pull julia@sha256:795c32c108c365c2480a69a195c9a7e377678d314eefe72f64c230c9178355af
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2083272778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe626ae4264c3793e3f2752abc204a549a77a114b9658003d2cda440332150c6`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Thu, 11 Jan 2024 00:02:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:02:52 GMT
ENV JULIA_VERSION=1.10.0
# Thu, 11 Jan 2024 00:02:53 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.0-win64.exe
# Thu, 11 Jan 2024 00:02:54 GMT
ENV JULIA_SHA256=f58aaa631748a5b0389586f3a3b7a081a2a6ac219a5a73a501ac61c0d99daebd
# Thu, 11 Jan 2024 00:04:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:04:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c4a7e196fc6ca93a61a3bbf497fb2b0eca327aa5cf473b95639f61b03c7c1d7`  
		Last Modified: Thu, 11 Jan 2024 00:04:09 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9346ba0550e4beb52f6dad09e1fa6fcd503e75c3df053e5648a54d6dfa7f05`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d7e35a894e972ab63511466519f9a4136a6144e7dbbd6e622be148046ddbaf`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e808d436d368c0aa304f09221c040769d471ae77d9fc07a9bad5a4eff093923`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86dd2e2e2c87845e244df41b72633372b4b9795242f069b3ab2ccbc728756ce8`  
		Last Modified: Thu, 11 Jan 2024 00:04:32 GMT  
		Size: 183.1 MB (183053648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c2cf5808cd6dced23f08a2d0921f88eae3754821b91d2df3decb5d5c8638a6`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1` - windows version 10.0.17763.5329; amd64

```console
$ docker pull julia@sha256:465739c99dd446c2698ee1f7151fc4f82c353749d9bc6b828a0e5e1db645c233
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2252827649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e690842a775a28bffae7fca39b8fa765ab792fabd7d6883bbc561866e2726e`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:03:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:03:43 GMT
ENV JULIA_VERSION=1.10.0
# Thu, 11 Jan 2024 00:03:44 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.0-win64.exe
# Thu, 11 Jan 2024 00:03:44 GMT
ENV JULIA_SHA256=f58aaa631748a5b0389586f3a3b7a081a2a6ac219a5a73a501ac61c0d99daebd
# Thu, 11 Jan 2024 00:05:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:05:27 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9e301d4f97511dcb9f3216268f983f8b8a38f59f6f47d7fcfa6c74bd89340c`  
		Last Modified: Thu, 11 Jan 2024 00:05:35 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15e9906d04250bd67cb869011a80e67292f17770b36865f9ce3b3f07765278f`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6305ccc6bbbc63d35ea2541315eff9b40ff82631ddc08cf97bae6597d416e35d`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fead423ba6e49e59afeb0485520bcfc1ca1f5231bc0104438c670c75c56d67a`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de60c693e3b77965993cdcd8ccef1ce49bbfd61e59f5e5f85a7b950645ce499b`  
		Last Modified: Thu, 11 Jan 2024 00:05:58 GMT  
		Size: 183.1 MB (183098483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ab8928320d6137aceb0a714f2cc037f1c072f50385773b2f6f1d39368da3fc`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-alpine`

```console
$ docker pull julia@sha256:15acea4c3855874b1349caf0600c7da2b05033ccfe67d0a8693edf814d1007e8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1-alpine` - linux; amd64

```console
$ docker pull julia@sha256:54a01c7689d514bf51a3494279a6877120729ed258de377f503d4782fca53bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176683112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432f75cca29ad8d3247b11295ee97b5a12c070431990e6180904f99400965b39`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["/bin/sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.0-musl-x86_64.tar.gz'; 			sha256='da8a9e0cf31eddd776276321802b9744acf5b8ce0171854b3e9d6394f656f9a2'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d8037af8d1d0f5fa4e82d16f39e0b5b2d7bb3071eeca07feddb80d63a9f084`  
		Last Modified: Sat, 27 Jan 2024 00:53:32 GMT  
		Size: 173.3 MB (173274017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534faee11eeb72a12ad121faf92d04078fb81e27ca029a61603381e7bfdade5c`  
		Last Modified: Sat, 27 Jan 2024 00:53:28 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-alpine` - unknown; unknown

```console
$ docker pull julia@sha256:4986f231ec2d9910a78844ccfbbedb86e0c958c6201d42a9a98f2e9208690dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.7 KB (83724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d769d8b51235a19931eb01c03a4bd6662cd2d79ec929b72c3ffd574289061c2a`

```dockerfile
```

-	Layers:
	-	`sha256:ba24d43b9b3ea2e4c533f1d19a970a9e97e8d6fdd95a182466235e35e952196e`  
		Last Modified: Sat, 27 Jan 2024 00:53:28 GMT  
		Size: 69.0 KB (69026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abe1763c27a7fb5692262541e30b12b927086a838ced1e6191ae3bdba7e05191`  
		Last Modified: Sat, 27 Jan 2024 00:53:28 GMT  
		Size: 14.7 KB (14698 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1-alpine3.18`

```console
$ docker pull julia@sha256:77a977b5edcfe0878250b81503abbe31f1425e64a0f12e1ada4d51b1da34758c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1-alpine3.18` - linux; amd64

```console
$ docker pull julia@sha256:5299d783ae55d8ef632b9cc263458d66a810a4de77a03ffae4e7fa820264aa53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176676774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee49bd257b2df90a18d0154e828326a5fcba99b347173d2169fe13bcd43dff0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["/bin/sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.0-musl-x86_64.tar.gz'; 			sha256='da8a9e0cf31eddd776276321802b9744acf5b8ce0171854b3e9d6394f656f9a2'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=alpine&os_version=3.18"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5204fc615595fd1ad835b0750c5fdb927818512d88052aef7e3850c09dd45475`  
		Last Modified: Sat, 27 Jan 2024 00:53:33 GMT  
		Size: 173.3 MB (173273866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3bd7244621863d2bbcbbe233abec587e6b376a86cab3eaec7803f2556e535f`  
		Last Modified: Sat, 27 Jan 2024 00:53:29 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-alpine3.18` - unknown; unknown

```console
$ docker pull julia@sha256:da0ca027e598e9773b125a066c844f5cefc1ecbbfb387e5b7661abd53bd31fe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 KB (80746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c093cd0eedbfc6980a82434ffc3879914906fc76b8f084df18d5c9012ffdb2aa`

```dockerfile
```

-	Layers:
	-	`sha256:58ec49d3d0285541a48ea975d3b7fdda895fc33f2c2d93c8933a42c1a3651f1a`  
		Last Modified: Sat, 27 Jan 2024 00:53:29 GMT  
		Size: 67.3 KB (67260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:187a1d23ed3a8d36572659404c674c1615b777fd9041abe5246a10eb10691ae7`  
		Last Modified: Sat, 27 Jan 2024 00:53:29 GMT  
		Size: 13.5 KB (13486 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1-alpine3.19`

```console
$ docker pull julia@sha256:15acea4c3855874b1349caf0600c7da2b05033ccfe67d0a8693edf814d1007e8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1-alpine3.19` - linux; amd64

```console
$ docker pull julia@sha256:54a01c7689d514bf51a3494279a6877120729ed258de377f503d4782fca53bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176683112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432f75cca29ad8d3247b11295ee97b5a12c070431990e6180904f99400965b39`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["/bin/sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.0-musl-x86_64.tar.gz'; 			sha256='da8a9e0cf31eddd776276321802b9744acf5b8ce0171854b3e9d6394f656f9a2'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d8037af8d1d0f5fa4e82d16f39e0b5b2d7bb3071eeca07feddb80d63a9f084`  
		Last Modified: Sat, 27 Jan 2024 00:53:32 GMT  
		Size: 173.3 MB (173274017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534faee11eeb72a12ad121faf92d04078fb81e27ca029a61603381e7bfdade5c`  
		Last Modified: Sat, 27 Jan 2024 00:53:28 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-alpine3.19` - unknown; unknown

```console
$ docker pull julia@sha256:4986f231ec2d9910a78844ccfbbedb86e0c958c6201d42a9a98f2e9208690dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.7 KB (83724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d769d8b51235a19931eb01c03a4bd6662cd2d79ec929b72c3ffd574289061c2a`

```dockerfile
```

-	Layers:
	-	`sha256:ba24d43b9b3ea2e4c533f1d19a970a9e97e8d6fdd95a182466235e35e952196e`  
		Last Modified: Sat, 27 Jan 2024 00:53:28 GMT  
		Size: 69.0 KB (69026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abe1763c27a7fb5692262541e30b12b927086a838ced1e6191ae3bdba7e05191`  
		Last Modified: Sat, 27 Jan 2024 00:53:28 GMT  
		Size: 14.7 KB (14698 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1-bookworm`

```console
$ docker pull julia@sha256:ae0f50e0d812f1537df24444125ca4b894e0e4a0e293b897b9ada6726f0ac007
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
$ docker pull julia@sha256:c581649ac221ebfbea9798a3bd66dfb0ba0dd44ba20ff5262d3c8bb93a759346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.9 MB (205909072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b184ca25c5acda81d0dc2e137ccf411bdd8e9f61fdd835d4bd55637d23b835`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad1c4eb009e797d65c1acfac69cd12c8f9060f29f760108f933027f2caab9c3`  
		Last Modified: Tue, 13 Feb 2024 01:53:54 GMT  
		Size: 5.7 MB (5707977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef8b6ee7f7fb149365afb062c086c37b5b314813fc6ec90095b002f5a925f0b`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 171.1 MB (171076635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d82177bdd251b5f04cc2ba1e5fd4efbafdbd4770a176a106cc21f400dbc05a`  
		Last Modified: Tue, 13 Feb 2024 01:53:54 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:3b5ca3771866b183000dca0a20d1bd2cb30d18b3a75d2ff32ac5cacaf423ef41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2158401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1bf8696406f25674e86fbc2d37065b3233c46aeb745f75fb02a0207775ca9a`

```dockerfile
```

-	Layers:
	-	`sha256:0884c94ffa8afd7175e4fdf92aa18f71815867215f0cde964240ba45b4f94154`  
		Last Modified: Tue, 13 Feb 2024 01:53:54 GMT  
		Size: 2.1 MB (2139045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:348b64f895c758148af65a9d8d6cf1581a93e955b08d7c118bee6923d2672bda`  
		Last Modified: Tue, 13 Feb 2024 01:53:54 GMT  
		Size: 19.4 KB (19356 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:c7b50eb125b7d60c63329a2c13798bc0c6e71611739c313a8ac466b505e9daab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199068374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc9cfd7eb49e87c970aa3df455f5951bd13608a351ad60fa41258f33c872dad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b14e605bd6638a1976eeb8d1cde59556a1f77295bac46d1669a9e27e6cd0ad6`  
		Last Modified: Wed, 14 Feb 2024 00:40:29 GMT  
		Size: 5.5 MB (5533149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d7d4913392d7182590a28188bd4fa882d0ed53f36bf9d49c1b5dfd74dda0ce`  
		Last Modified: Wed, 14 Feb 2024 00:40:32 GMT  
		Size: 164.4 MB (164378492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c05a2fc2483ea3c18ac5829c7ca9c7c9fd40204cb09b4ace74a3c02cb27dbe9`  
		Last Modified: Wed, 14 Feb 2024 00:40:28 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:7812cc45c880626d2dfa14638dfc0dcca6d09a54e1b49abf8d917a8f8a6fd61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2157622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d96f6d9b1c89aaf182d67e03efcae208a6f69ae643a004df4c24d36a84b881f`

```dockerfile
```

-	Layers:
	-	`sha256:ffca818dcaa241a02e65213ba00b90e138a6c248aaa839bb326ddf81d27472f1`  
		Last Modified: Wed, 14 Feb 2024 00:40:29 GMT  
		Size: 2.1 MB (2138415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7b32281e96ad074af12b3d2e1fec978b2b8afb5106ab0eeb89189cedc13c81d`  
		Last Modified: Wed, 14 Feb 2024 00:40:29 GMT  
		Size: 19.2 KB (19207 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; 386

```console
$ docker pull julia@sha256:ed5dae7c246f3779da0892e59fefc8a2a06c1b0418c75cc66df890b64fbd5d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192476013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266a487238b5f50dc9dd3bc262639f4da7f6d7b6194a3f48742cf1725df03675`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adcfe329152d3631bed65ca802c4d591cf2466ececc127b4689e12fd044b6dd9`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 5.9 MB (5863232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7f556d75a67e2c4d02467097026cac3136c670701b05d1fe37c2209b150c66`  
		Last Modified: Tue, 13 Feb 2024 01:53:58 GMT  
		Size: 156.5 MB (156470603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee51a4a243b601cbdaea50eb3df43c6297660d3956259740ebcbb63126d2d0a`  
		Last Modified: Tue, 13 Feb 2024 01:53:54 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:98bc5d459492dc920f2634c7d2a39252f464f40045e8ee9bb9a967df561e7fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2155528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741936c96e550374e6be8d4320cd5b8e3cf1b315e382afac934f7edfc2236eb3`

```dockerfile
```

-	Layers:
	-	`sha256:53aa4312033ace4a7cf6f547e9085d8bd6890df5b2615d784fc182399ed92297`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 2.1 MB (2136223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3060f20bd073e1f89280df62e40daa82ac66677706d6628b0e7ce70250402b51`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 19.3 KB (19305 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:42518fad4d8a20363e408d6bf3ce4259a1203bc1f3a1720ede05055daf233cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.3 MB (193349040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc361617127c03f5ef43a89da3fa93390c1213068a6e940b721330dc4e63a12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:b65bdf3d9277efbf6bbf8bf0121f92bdcd342ed0c4f49f1cee3b91adafacd76c in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b1cce6d9947985e4270ac998aa258401bc5deca94d504040a14f9f3c47258d68`  
		Last Modified: Tue, 13 Feb 2024 00:43:56 GMT  
		Size: 33.1 MB (33118908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a48b566372cb4fa0fec129e803c39a28de529b9736fd03a42344641249c1fc`  
		Last Modified: Tue, 13 Feb 2024 21:54:44 GMT  
		Size: 6.2 MB (6239799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85e6dfe440366f653bf664315e491fe0cb2bb189428018fbcf657460fbbc3fa`  
		Last Modified: Tue, 13 Feb 2024 21:54:47 GMT  
		Size: 154.0 MB (153989961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6306b805ea4661e164d23cfd0d8dfae9d27c498477a790d3351d0f6ecc3e5fd`  
		Last Modified: Tue, 13 Feb 2024 21:54:43 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:8ed461f46641215c54d31c67c06954851c85f63b1d2b4eebe9351ecff9289da9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2161862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286b8e56e5b1f465b474b30b2fe8512b0c2238bef520a8bd95c4e5e31b59df2c`

```dockerfile
```

-	Layers:
	-	`sha256:9da0b3fffb06b598b8c17e331a4e70d4e6b54c5bfad5a40d4e88a16d3966ab41`  
		Last Modified: Tue, 13 Feb 2024 21:54:43 GMT  
		Size: 2.1 MB (2142609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbfe360df232fd616240d3f8aae495b7a956d6a7383dcdf4dc8ae56cd7d319c2`  
		Last Modified: Tue, 13 Feb 2024 21:54:43 GMT  
		Size: 19.3 KB (19253 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1-bullseye`

```console
$ docker pull julia@sha256:f6dd1793015df42b577c0375b98514ba7979171f5957bb0e475aa3539ef21d5d
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

### `julia:1-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:8d384ae00c7c02cbee899728190fcdd1faca693ec80fed6d734c76a84922a118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 MB (204925804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19950a8b05c384b4f92d751f4f10a98e63aa069ead4d5cf9186b030c920da3a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f3f6d4871c74f7b63e34b697a9aaefa8835f1889dc6903866338a86317002e`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 2.4 MB (2426534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba72295cd998aea9729c2a415acf7f007a528c2b4d6f1c34387bb92d9bac746`  
		Last Modified: Tue, 13 Feb 2024 01:53:58 GMT  
		Size: 171.1 MB (171076476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d0425419406b5a1143dff3543f91ff035c7d0ecb9bf0774e64e01554e02e20`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:8273a9fdda9b316a362eeb3ea1e578ee9092b278a30a718754a7c3a8deacd3e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04952d04716e6ab86f7cf6f5e35bd7873721540b5380dd2811279304f811d7f4`

```dockerfile
```

-	Layers:
	-	`sha256:432180086c941804e7ee5fcf6bd251520e95f0fdb359e58e157794fe17baa0b4`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 2.4 MB (2359551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:870a84f47d45ed4bb0321a5cc4914f58d0ee37c40ea0d352c1b840eaa8d48cca`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 18.2 KB (18186 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:5487dbd9e86ea6dfdde1e83477c820ef9096cbd52e19dcc574b6fd9efb76b2ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.9 MB (196864925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80daa6ec8fc78a3eec97067ae5b96e344d99367cccefba598286c51b1386fdf0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1acd381bc5ce074386a44640a70f3d2d53921e7cda7c6386a20616c9fab4cee5`  
		Last Modified: Wed, 14 Feb 2024 00:41:34 GMT  
		Size: 2.4 MB (2415040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520a7f557218cd3b5ef3f4ddd5afcca8d80438c186a9bf2521eda165facd2c91`  
		Last Modified: Wed, 14 Feb 2024 00:41:38 GMT  
		Size: 164.4 MB (164378442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:268a60e13473050784334fa5d0cc23da2209b45f3251f0133c2c05c309d0b752`  
		Last Modified: Wed, 14 Feb 2024 00:41:33 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:f8bb44f08113f3d1137034416ccf2f473631f08424eb97007061de4ac057ae2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2376931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:951d6f2d9e6a3d58bcd7de98a60c4417e42eeafb974b36e71f6fb0760357a357`

```dockerfile
```

-	Layers:
	-	`sha256:7beff45e48bb073460b5214a082784914cd78b5c8864627f675670dff6784190`  
		Last Modified: Wed, 14 Feb 2024 00:41:34 GMT  
		Size: 2.4 MB (2358903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2687ab055e0cc2332a76ad9df388d45043b631992252746a3b6d1260836fc41`  
		Last Modified: Wed, 14 Feb 2024 00:41:34 GMT  
		Size: 18.0 KB (18028 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bullseye` - linux; 386

```console
$ docker pull julia@sha256:3348a4e15f9eb821e27b64f594aee5b549605b9a02ce2d81bf0296660348dccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191411992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34cc23d0f384f592a3f59a3d676eb76d72ea43b54725d5f8e0baeb644aebdffb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:9eaee5af136d095dc1dac0ffce0fde09d8f1bd02ff7cb65ee67e00b2a66f34f7 in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1ac8173b08d16f9f136fb0e3ee39999cef7495f924ecb43f3ca4a4eea267cc88`  
		Last Modified: Tue, 13 Feb 2024 00:44:36 GMT  
		Size: 32.4 MB (32407443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf492369ec4d56d2010213bf0c01a1d0be40c950eda27da51921ed8c2a1bc09`  
		Last Modified: Tue, 13 Feb 2024 01:53:53 GMT  
		Size: 2.5 MB (2533067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7d0f5baeea89d7b49c54cc577eab3867247693f466f98b3cc4f2399efcb0af`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 156.5 MB (156471113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6be2aecc9dc90a8f90619365daf78c2fc8f2c67056592b5b10683e9b84c892`  
		Last Modified: Tue, 13 Feb 2024 01:53:53 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:8016124e8b1742e9b8063df61bae834e255e72ef863ed54fde680195b00a6e09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2374912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9820be04702fdac240a66ebb9fed36ff9a01b291501d69df9966aaa79cbb048`

```dockerfile
```

-	Layers:
	-	`sha256:b5b0fa0ccbf3afd955632b36296386d1988c6a60b808e7101b4b3f9320935cd2`  
		Last Modified: Tue, 13 Feb 2024 01:53:53 GMT  
		Size: 2.4 MB (2356757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:427416a00deb6fc64dea6ac42ea75526fa410b61d0f98ed7c269e848697a670b`  
		Last Modified: Tue, 13 Feb 2024 01:53:53 GMT  
		Size: 18.2 KB (18155 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bullseye` - linux; ppc64le

```console
$ docker pull julia@sha256:34e38bddb83d3e554661ccd943af43cdb864af337b665e80d319d17641dcae38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.9 MB (191918984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce2e008edde3927a13f00754ee8f8a138c1cccfbf871fbecc2c26aa365977fee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:f8e53a63f5fbfb32b4bac66dc2b16f2e2d101e5feb6cd9e3b6d3065fb8aee14d in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5c87ba6a2e42f083a6cfdea0d3b1b3bc977a5065ff0087fdbf4fc8dbc7982a38`  
		Last Modified: Tue, 13 Feb 2024 00:44:50 GMT  
		Size: 35.3 MB (35297799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc406362a4b5aed4760caff7c4bc06a04cb2bd3834a923f056a5baf70eb0d7ff`  
		Last Modified: Tue, 13 Feb 2024 21:56:31 GMT  
		Size: 2.6 MB (2629991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278b4e0551a3587b5d022b566e56d527b968803375aa151bdd2dc6d30b7c7813`  
		Last Modified: Tue, 13 Feb 2024 21:56:34 GMT  
		Size: 154.0 MB (153990822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a158664e796ca3ee0566bb6b7e2b79e13c3161c9f36f6dadb04bf7cdcbb6e58`  
		Last Modified: Tue, 13 Feb 2024 21:56:30 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:074faa55f685aff95e390f40bbece0962016efb2de45e76932ad7ec77379eb75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adae430aa8a2857fe05d29dfd22203f96e4ba41334491bf64c9bcf168e2689ce`

```dockerfile
```

-	Layers:
	-	`sha256:a3834b7b363b094f8ccc42c1d8c1266c29a4d88ab2002bc4a6d745aef0871e7b`  
		Last Modified: Tue, 13 Feb 2024 21:56:30 GMT  
		Size: 2.4 MB (2363081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22fd53c802c699b2d4eec0a68f896ffad71210add2b28509849ee2d177075647`  
		Last Modified: Tue, 13 Feb 2024 21:56:30 GMT  
		Size: 18.1 KB (18059 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1-windowsservercore`

```console
$ docker pull julia@sha256:e0173a4d8892b7b6234c3d97cc83366460fefb0737c3333da0fda52b9f2fe0c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `julia:1-windowsservercore` - windows version 10.0.20348.2227; amd64

```console
$ docker pull julia@sha256:795c32c108c365c2480a69a195c9a7e377678d314eefe72f64c230c9178355af
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2083272778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe626ae4264c3793e3f2752abc204a549a77a114b9658003d2cda440332150c6`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Thu, 11 Jan 2024 00:02:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:02:52 GMT
ENV JULIA_VERSION=1.10.0
# Thu, 11 Jan 2024 00:02:53 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.0-win64.exe
# Thu, 11 Jan 2024 00:02:54 GMT
ENV JULIA_SHA256=f58aaa631748a5b0389586f3a3b7a081a2a6ac219a5a73a501ac61c0d99daebd
# Thu, 11 Jan 2024 00:04:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:04:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c4a7e196fc6ca93a61a3bbf497fb2b0eca327aa5cf473b95639f61b03c7c1d7`  
		Last Modified: Thu, 11 Jan 2024 00:04:09 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9346ba0550e4beb52f6dad09e1fa6fcd503e75c3df053e5648a54d6dfa7f05`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d7e35a894e972ab63511466519f9a4136a6144e7dbbd6e622be148046ddbaf`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e808d436d368c0aa304f09221c040769d471ae77d9fc07a9bad5a4eff093923`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86dd2e2e2c87845e244df41b72633372b4b9795242f069b3ab2ccbc728756ce8`  
		Last Modified: Thu, 11 Jan 2024 00:04:32 GMT  
		Size: 183.1 MB (183053648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c2cf5808cd6dced23f08a2d0921f88eae3754821b91d2df3decb5d5c8638a6`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-windowsservercore` - windows version 10.0.17763.5329; amd64

```console
$ docker pull julia@sha256:465739c99dd446c2698ee1f7151fc4f82c353749d9bc6b828a0e5e1db645c233
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2252827649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e690842a775a28bffae7fca39b8fa765ab792fabd7d6883bbc561866e2726e`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:03:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:03:43 GMT
ENV JULIA_VERSION=1.10.0
# Thu, 11 Jan 2024 00:03:44 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.0-win64.exe
# Thu, 11 Jan 2024 00:03:44 GMT
ENV JULIA_SHA256=f58aaa631748a5b0389586f3a3b7a081a2a6ac219a5a73a501ac61c0d99daebd
# Thu, 11 Jan 2024 00:05:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:05:27 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9e301d4f97511dcb9f3216268f983f8b8a38f59f6f47d7fcfa6c74bd89340c`  
		Last Modified: Thu, 11 Jan 2024 00:05:35 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15e9906d04250bd67cb869011a80e67292f17770b36865f9ce3b3f07765278f`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6305ccc6bbbc63d35ea2541315eff9b40ff82631ddc08cf97bae6597d416e35d`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fead423ba6e49e59afeb0485520bcfc1ca1f5231bc0104438c670c75c56d67a`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de60c693e3b77965993cdcd8ccef1ce49bbfd61e59f5e5f85a7b950645ce499b`  
		Last Modified: Thu, 11 Jan 2024 00:05:58 GMT  
		Size: 183.1 MB (183098483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ab8928320d6137aceb0a714f2cc037f1c072f50385773b2f6f1d39368da3fc`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore-1809`

```console
$ docker pull julia@sha256:999bd26e0d2f8bf19acbc55dbda3f7303d67f591de5cfdfe5a04914cc44d8c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `julia:1-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull julia@sha256:465739c99dd446c2698ee1f7151fc4f82c353749d9bc6b828a0e5e1db645c233
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2252827649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e690842a775a28bffae7fca39b8fa765ab792fabd7d6883bbc561866e2726e`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:03:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:03:43 GMT
ENV JULIA_VERSION=1.10.0
# Thu, 11 Jan 2024 00:03:44 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.0-win64.exe
# Thu, 11 Jan 2024 00:03:44 GMT
ENV JULIA_SHA256=f58aaa631748a5b0389586f3a3b7a081a2a6ac219a5a73a501ac61c0d99daebd
# Thu, 11 Jan 2024 00:05:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:05:27 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9e301d4f97511dcb9f3216268f983f8b8a38f59f6f47d7fcfa6c74bd89340c`  
		Last Modified: Thu, 11 Jan 2024 00:05:35 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15e9906d04250bd67cb869011a80e67292f17770b36865f9ce3b3f07765278f`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6305ccc6bbbc63d35ea2541315eff9b40ff82631ddc08cf97bae6597d416e35d`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fead423ba6e49e59afeb0485520bcfc1ca1f5231bc0104438c670c75c56d67a`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de60c693e3b77965993cdcd8ccef1ce49bbfd61e59f5e5f85a7b950645ce499b`  
		Last Modified: Thu, 11 Jan 2024 00:05:58 GMT  
		Size: 183.1 MB (183098483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ab8928320d6137aceb0a714f2cc037f1c072f50385773b2f6f1d39368da3fc`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:473983fe5fe55383db5d0d11749bebef8288fe2bc9eb5a72ab3f76b3e6c45d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `julia:1-windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull julia@sha256:795c32c108c365c2480a69a195c9a7e377678d314eefe72f64c230c9178355af
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2083272778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe626ae4264c3793e3f2752abc204a549a77a114b9658003d2cda440332150c6`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Thu, 11 Jan 2024 00:02:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:02:52 GMT
ENV JULIA_VERSION=1.10.0
# Thu, 11 Jan 2024 00:02:53 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.0-win64.exe
# Thu, 11 Jan 2024 00:02:54 GMT
ENV JULIA_SHA256=f58aaa631748a5b0389586f3a3b7a081a2a6ac219a5a73a501ac61c0d99daebd
# Thu, 11 Jan 2024 00:04:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:04:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c4a7e196fc6ca93a61a3bbf497fb2b0eca327aa5cf473b95639f61b03c7c1d7`  
		Last Modified: Thu, 11 Jan 2024 00:04:09 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9346ba0550e4beb52f6dad09e1fa6fcd503e75c3df053e5648a54d6dfa7f05`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d7e35a894e972ab63511466519f9a4136a6144e7dbbd6e622be148046ddbaf`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e808d436d368c0aa304f09221c040769d471ae77d9fc07a9bad5a4eff093923`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86dd2e2e2c87845e244df41b72633372b4b9795242f069b3ab2ccbc728756ce8`  
		Last Modified: Thu, 11 Jan 2024 00:04:32 GMT  
		Size: 183.1 MB (183053648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c2cf5808cd6dced23f08a2d0921f88eae3754821b91d2df3decb5d5c8638a6`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10`

```console
$ docker pull julia@sha256:564460379e4782890dbfe5f073481eceb044b96cefb69f45805f9901fee5a747
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
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `julia:1.10` - linux; amd64

```console
$ docker pull julia@sha256:c581649ac221ebfbea9798a3bd66dfb0ba0dd44ba20ff5262d3c8bb93a759346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.9 MB (205909072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b184ca25c5acda81d0dc2e137ccf411bdd8e9f61fdd835d4bd55637d23b835`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad1c4eb009e797d65c1acfac69cd12c8f9060f29f760108f933027f2caab9c3`  
		Last Modified: Tue, 13 Feb 2024 01:53:54 GMT  
		Size: 5.7 MB (5707977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef8b6ee7f7fb149365afb062c086c37b5b314813fc6ec90095b002f5a925f0b`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 171.1 MB (171076635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d82177bdd251b5f04cc2ba1e5fd4efbafdbd4770a176a106cc21f400dbc05a`  
		Last Modified: Tue, 13 Feb 2024 01:53:54 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:3b5ca3771866b183000dca0a20d1bd2cb30d18b3a75d2ff32ac5cacaf423ef41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2158401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1bf8696406f25674e86fbc2d37065b3233c46aeb745f75fb02a0207775ca9a`

```dockerfile
```

-	Layers:
	-	`sha256:0884c94ffa8afd7175e4fdf92aa18f71815867215f0cde964240ba45b4f94154`  
		Last Modified: Tue, 13 Feb 2024 01:53:54 GMT  
		Size: 2.1 MB (2139045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:348b64f895c758148af65a9d8d6cf1581a93e955b08d7c118bee6923d2672bda`  
		Last Modified: Tue, 13 Feb 2024 01:53:54 GMT  
		Size: 19.4 KB (19356 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:c7b50eb125b7d60c63329a2c13798bc0c6e71611739c313a8ac466b505e9daab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199068374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc9cfd7eb49e87c970aa3df455f5951bd13608a351ad60fa41258f33c872dad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b14e605bd6638a1976eeb8d1cde59556a1f77295bac46d1669a9e27e6cd0ad6`  
		Last Modified: Wed, 14 Feb 2024 00:40:29 GMT  
		Size: 5.5 MB (5533149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d7d4913392d7182590a28188bd4fa882d0ed53f36bf9d49c1b5dfd74dda0ce`  
		Last Modified: Wed, 14 Feb 2024 00:40:32 GMT  
		Size: 164.4 MB (164378492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c05a2fc2483ea3c18ac5829c7ca9c7c9fd40204cb09b4ace74a3c02cb27dbe9`  
		Last Modified: Wed, 14 Feb 2024 00:40:28 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:7812cc45c880626d2dfa14638dfc0dcca6d09a54e1b49abf8d917a8f8a6fd61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2157622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d96f6d9b1c89aaf182d67e03efcae208a6f69ae643a004df4c24d36a84b881f`

```dockerfile
```

-	Layers:
	-	`sha256:ffca818dcaa241a02e65213ba00b90e138a6c248aaa839bb326ddf81d27472f1`  
		Last Modified: Wed, 14 Feb 2024 00:40:29 GMT  
		Size: 2.1 MB (2138415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7b32281e96ad074af12b3d2e1fec978b2b8afb5106ab0eeb89189cedc13c81d`  
		Last Modified: Wed, 14 Feb 2024 00:40:29 GMT  
		Size: 19.2 KB (19207 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; 386

```console
$ docker pull julia@sha256:ed5dae7c246f3779da0892e59fefc8a2a06c1b0418c75cc66df890b64fbd5d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192476013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266a487238b5f50dc9dd3bc262639f4da7f6d7b6194a3f48742cf1725df03675`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adcfe329152d3631bed65ca802c4d591cf2466ececc127b4689e12fd044b6dd9`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 5.9 MB (5863232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7f556d75a67e2c4d02467097026cac3136c670701b05d1fe37c2209b150c66`  
		Last Modified: Tue, 13 Feb 2024 01:53:58 GMT  
		Size: 156.5 MB (156470603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee51a4a243b601cbdaea50eb3df43c6297660d3956259740ebcbb63126d2d0a`  
		Last Modified: Tue, 13 Feb 2024 01:53:54 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:98bc5d459492dc920f2634c7d2a39252f464f40045e8ee9bb9a967df561e7fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2155528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741936c96e550374e6be8d4320cd5b8e3cf1b315e382afac934f7edfc2236eb3`

```dockerfile
```

-	Layers:
	-	`sha256:53aa4312033ace4a7cf6f547e9085d8bd6890df5b2615d784fc182399ed92297`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 2.1 MB (2136223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3060f20bd073e1f89280df62e40daa82ac66677706d6628b0e7ce70250402b51`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 19.3 KB (19305 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; ppc64le

```console
$ docker pull julia@sha256:42518fad4d8a20363e408d6bf3ce4259a1203bc1f3a1720ede05055daf233cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.3 MB (193349040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc361617127c03f5ef43a89da3fa93390c1213068a6e940b721330dc4e63a12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:b65bdf3d9277efbf6bbf8bf0121f92bdcd342ed0c4f49f1cee3b91adafacd76c in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b1cce6d9947985e4270ac998aa258401bc5deca94d504040a14f9f3c47258d68`  
		Last Modified: Tue, 13 Feb 2024 00:43:56 GMT  
		Size: 33.1 MB (33118908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a48b566372cb4fa0fec129e803c39a28de529b9736fd03a42344641249c1fc`  
		Last Modified: Tue, 13 Feb 2024 21:54:44 GMT  
		Size: 6.2 MB (6239799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85e6dfe440366f653bf664315e491fe0cb2bb189428018fbcf657460fbbc3fa`  
		Last Modified: Tue, 13 Feb 2024 21:54:47 GMT  
		Size: 154.0 MB (153989961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6306b805ea4661e164d23cfd0d8dfae9d27c498477a790d3351d0f6ecc3e5fd`  
		Last Modified: Tue, 13 Feb 2024 21:54:43 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:8ed461f46641215c54d31c67c06954851c85f63b1d2b4eebe9351ecff9289da9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2161862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286b8e56e5b1f465b474b30b2fe8512b0c2238bef520a8bd95c4e5e31b59df2c`

```dockerfile
```

-	Layers:
	-	`sha256:9da0b3fffb06b598b8c17e331a4e70d4e6b54c5bfad5a40d4e88a16d3966ab41`  
		Last Modified: Tue, 13 Feb 2024 21:54:43 GMT  
		Size: 2.1 MB (2142609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbfe360df232fd616240d3f8aae495b7a956d6a7383dcdf4dc8ae56cd7d319c2`  
		Last Modified: Tue, 13 Feb 2024 21:54:43 GMT  
		Size: 19.3 KB (19253 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - windows version 10.0.20348.2227; amd64

```console
$ docker pull julia@sha256:795c32c108c365c2480a69a195c9a7e377678d314eefe72f64c230c9178355af
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2083272778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe626ae4264c3793e3f2752abc204a549a77a114b9658003d2cda440332150c6`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Thu, 11 Jan 2024 00:02:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:02:52 GMT
ENV JULIA_VERSION=1.10.0
# Thu, 11 Jan 2024 00:02:53 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.0-win64.exe
# Thu, 11 Jan 2024 00:02:54 GMT
ENV JULIA_SHA256=f58aaa631748a5b0389586f3a3b7a081a2a6ac219a5a73a501ac61c0d99daebd
# Thu, 11 Jan 2024 00:04:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:04:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c4a7e196fc6ca93a61a3bbf497fb2b0eca327aa5cf473b95639f61b03c7c1d7`  
		Last Modified: Thu, 11 Jan 2024 00:04:09 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9346ba0550e4beb52f6dad09e1fa6fcd503e75c3df053e5648a54d6dfa7f05`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d7e35a894e972ab63511466519f9a4136a6144e7dbbd6e622be148046ddbaf`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e808d436d368c0aa304f09221c040769d471ae77d9fc07a9bad5a4eff093923`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86dd2e2e2c87845e244df41b72633372b4b9795242f069b3ab2ccbc728756ce8`  
		Last Modified: Thu, 11 Jan 2024 00:04:32 GMT  
		Size: 183.1 MB (183053648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c2cf5808cd6dced23f08a2d0921f88eae3754821b91d2df3decb5d5c8638a6`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10` - windows version 10.0.17763.5329; amd64

```console
$ docker pull julia@sha256:465739c99dd446c2698ee1f7151fc4f82c353749d9bc6b828a0e5e1db645c233
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2252827649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e690842a775a28bffae7fca39b8fa765ab792fabd7d6883bbc561866e2726e`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:03:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:03:43 GMT
ENV JULIA_VERSION=1.10.0
# Thu, 11 Jan 2024 00:03:44 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.0-win64.exe
# Thu, 11 Jan 2024 00:03:44 GMT
ENV JULIA_SHA256=f58aaa631748a5b0389586f3a3b7a081a2a6ac219a5a73a501ac61c0d99daebd
# Thu, 11 Jan 2024 00:05:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:05:27 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9e301d4f97511dcb9f3216268f983f8b8a38f59f6f47d7fcfa6c74bd89340c`  
		Last Modified: Thu, 11 Jan 2024 00:05:35 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15e9906d04250bd67cb869011a80e67292f17770b36865f9ce3b3f07765278f`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6305ccc6bbbc63d35ea2541315eff9b40ff82631ddc08cf97bae6597d416e35d`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fead423ba6e49e59afeb0485520bcfc1ca1f5231bc0104438c670c75c56d67a`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de60c693e3b77965993cdcd8ccef1ce49bbfd61e59f5e5f85a7b950645ce499b`  
		Last Modified: Thu, 11 Jan 2024 00:05:58 GMT  
		Size: 183.1 MB (183098483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ab8928320d6137aceb0a714f2cc037f1c072f50385773b2f6f1d39368da3fc`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-alpine`

```console
$ docker pull julia@sha256:15acea4c3855874b1349caf0600c7da2b05033ccfe67d0a8693edf814d1007e8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10-alpine` - linux; amd64

```console
$ docker pull julia@sha256:54a01c7689d514bf51a3494279a6877120729ed258de377f503d4782fca53bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176683112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432f75cca29ad8d3247b11295ee97b5a12c070431990e6180904f99400965b39`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["/bin/sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.0-musl-x86_64.tar.gz'; 			sha256='da8a9e0cf31eddd776276321802b9744acf5b8ce0171854b3e9d6394f656f9a2'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d8037af8d1d0f5fa4e82d16f39e0b5b2d7bb3071eeca07feddb80d63a9f084`  
		Last Modified: Sat, 27 Jan 2024 00:53:32 GMT  
		Size: 173.3 MB (173274017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534faee11eeb72a12ad121faf92d04078fb81e27ca029a61603381e7bfdade5c`  
		Last Modified: Sat, 27 Jan 2024 00:53:28 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-alpine` - unknown; unknown

```console
$ docker pull julia@sha256:4986f231ec2d9910a78844ccfbbedb86e0c958c6201d42a9a98f2e9208690dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.7 KB (83724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d769d8b51235a19931eb01c03a4bd6662cd2d79ec929b72c3ffd574289061c2a`

```dockerfile
```

-	Layers:
	-	`sha256:ba24d43b9b3ea2e4c533f1d19a970a9e97e8d6fdd95a182466235e35e952196e`  
		Last Modified: Sat, 27 Jan 2024 00:53:28 GMT  
		Size: 69.0 KB (69026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abe1763c27a7fb5692262541e30b12b927086a838ced1e6191ae3bdba7e05191`  
		Last Modified: Sat, 27 Jan 2024 00:53:28 GMT  
		Size: 14.7 KB (14698 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-alpine3.18`

```console
$ docker pull julia@sha256:77a977b5edcfe0878250b81503abbe31f1425e64a0f12e1ada4d51b1da34758c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10-alpine3.18` - linux; amd64

```console
$ docker pull julia@sha256:5299d783ae55d8ef632b9cc263458d66a810a4de77a03ffae4e7fa820264aa53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176676774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee49bd257b2df90a18d0154e828326a5fcba99b347173d2169fe13bcd43dff0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["/bin/sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.0-musl-x86_64.tar.gz'; 			sha256='da8a9e0cf31eddd776276321802b9744acf5b8ce0171854b3e9d6394f656f9a2'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=alpine&os_version=3.18"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5204fc615595fd1ad835b0750c5fdb927818512d88052aef7e3850c09dd45475`  
		Last Modified: Sat, 27 Jan 2024 00:53:33 GMT  
		Size: 173.3 MB (173273866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3bd7244621863d2bbcbbe233abec587e6b376a86cab3eaec7803f2556e535f`  
		Last Modified: Sat, 27 Jan 2024 00:53:29 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-alpine3.18` - unknown; unknown

```console
$ docker pull julia@sha256:da0ca027e598e9773b125a066c844f5cefc1ecbbfb387e5b7661abd53bd31fe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 KB (80746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c093cd0eedbfc6980a82434ffc3879914906fc76b8f084df18d5c9012ffdb2aa`

```dockerfile
```

-	Layers:
	-	`sha256:58ec49d3d0285541a48ea975d3b7fdda895fc33f2c2d93c8933a42c1a3651f1a`  
		Last Modified: Sat, 27 Jan 2024 00:53:29 GMT  
		Size: 67.3 KB (67260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:187a1d23ed3a8d36572659404c674c1615b777fd9041abe5246a10eb10691ae7`  
		Last Modified: Sat, 27 Jan 2024 00:53:29 GMT  
		Size: 13.5 KB (13486 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-alpine3.19`

```console
$ docker pull julia@sha256:15acea4c3855874b1349caf0600c7da2b05033ccfe67d0a8693edf814d1007e8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10-alpine3.19` - linux; amd64

```console
$ docker pull julia@sha256:54a01c7689d514bf51a3494279a6877120729ed258de377f503d4782fca53bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176683112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432f75cca29ad8d3247b11295ee97b5a12c070431990e6180904f99400965b39`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["/bin/sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.0-musl-x86_64.tar.gz'; 			sha256='da8a9e0cf31eddd776276321802b9744acf5b8ce0171854b3e9d6394f656f9a2'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d8037af8d1d0f5fa4e82d16f39e0b5b2d7bb3071eeca07feddb80d63a9f084`  
		Last Modified: Sat, 27 Jan 2024 00:53:32 GMT  
		Size: 173.3 MB (173274017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534faee11eeb72a12ad121faf92d04078fb81e27ca029a61603381e7bfdade5c`  
		Last Modified: Sat, 27 Jan 2024 00:53:28 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-alpine3.19` - unknown; unknown

```console
$ docker pull julia@sha256:4986f231ec2d9910a78844ccfbbedb86e0c958c6201d42a9a98f2e9208690dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.7 KB (83724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d769d8b51235a19931eb01c03a4bd6662cd2d79ec929b72c3ffd574289061c2a`

```dockerfile
```

-	Layers:
	-	`sha256:ba24d43b9b3ea2e4c533f1d19a970a9e97e8d6fdd95a182466235e35e952196e`  
		Last Modified: Sat, 27 Jan 2024 00:53:28 GMT  
		Size: 69.0 KB (69026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abe1763c27a7fb5692262541e30b12b927086a838ced1e6191ae3bdba7e05191`  
		Last Modified: Sat, 27 Jan 2024 00:53:28 GMT  
		Size: 14.7 KB (14698 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-bookworm`

```console
$ docker pull julia@sha256:ae0f50e0d812f1537df24444125ca4b894e0e4a0e293b897b9ada6726f0ac007
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
$ docker pull julia@sha256:c581649ac221ebfbea9798a3bd66dfb0ba0dd44ba20ff5262d3c8bb93a759346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.9 MB (205909072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b184ca25c5acda81d0dc2e137ccf411bdd8e9f61fdd835d4bd55637d23b835`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad1c4eb009e797d65c1acfac69cd12c8f9060f29f760108f933027f2caab9c3`  
		Last Modified: Tue, 13 Feb 2024 01:53:54 GMT  
		Size: 5.7 MB (5707977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef8b6ee7f7fb149365afb062c086c37b5b314813fc6ec90095b002f5a925f0b`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 171.1 MB (171076635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d82177bdd251b5f04cc2ba1e5fd4efbafdbd4770a176a106cc21f400dbc05a`  
		Last Modified: Tue, 13 Feb 2024 01:53:54 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:3b5ca3771866b183000dca0a20d1bd2cb30d18b3a75d2ff32ac5cacaf423ef41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2158401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1bf8696406f25674e86fbc2d37065b3233c46aeb745f75fb02a0207775ca9a`

```dockerfile
```

-	Layers:
	-	`sha256:0884c94ffa8afd7175e4fdf92aa18f71815867215f0cde964240ba45b4f94154`  
		Last Modified: Tue, 13 Feb 2024 01:53:54 GMT  
		Size: 2.1 MB (2139045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:348b64f895c758148af65a9d8d6cf1581a93e955b08d7c118bee6923d2672bda`  
		Last Modified: Tue, 13 Feb 2024 01:53:54 GMT  
		Size: 19.4 KB (19356 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:c7b50eb125b7d60c63329a2c13798bc0c6e71611739c313a8ac466b505e9daab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199068374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc9cfd7eb49e87c970aa3df455f5951bd13608a351ad60fa41258f33c872dad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b14e605bd6638a1976eeb8d1cde59556a1f77295bac46d1669a9e27e6cd0ad6`  
		Last Modified: Wed, 14 Feb 2024 00:40:29 GMT  
		Size: 5.5 MB (5533149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d7d4913392d7182590a28188bd4fa882d0ed53f36bf9d49c1b5dfd74dda0ce`  
		Last Modified: Wed, 14 Feb 2024 00:40:32 GMT  
		Size: 164.4 MB (164378492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c05a2fc2483ea3c18ac5829c7ca9c7c9fd40204cb09b4ace74a3c02cb27dbe9`  
		Last Modified: Wed, 14 Feb 2024 00:40:28 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:7812cc45c880626d2dfa14638dfc0dcca6d09a54e1b49abf8d917a8f8a6fd61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2157622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d96f6d9b1c89aaf182d67e03efcae208a6f69ae643a004df4c24d36a84b881f`

```dockerfile
```

-	Layers:
	-	`sha256:ffca818dcaa241a02e65213ba00b90e138a6c248aaa839bb326ddf81d27472f1`  
		Last Modified: Wed, 14 Feb 2024 00:40:29 GMT  
		Size: 2.1 MB (2138415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7b32281e96ad074af12b3d2e1fec978b2b8afb5106ab0eeb89189cedc13c81d`  
		Last Modified: Wed, 14 Feb 2024 00:40:29 GMT  
		Size: 19.2 KB (19207 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; 386

```console
$ docker pull julia@sha256:ed5dae7c246f3779da0892e59fefc8a2a06c1b0418c75cc66df890b64fbd5d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192476013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266a487238b5f50dc9dd3bc262639f4da7f6d7b6194a3f48742cf1725df03675`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adcfe329152d3631bed65ca802c4d591cf2466ececc127b4689e12fd044b6dd9`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 5.9 MB (5863232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7f556d75a67e2c4d02467097026cac3136c670701b05d1fe37c2209b150c66`  
		Last Modified: Tue, 13 Feb 2024 01:53:58 GMT  
		Size: 156.5 MB (156470603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee51a4a243b601cbdaea50eb3df43c6297660d3956259740ebcbb63126d2d0a`  
		Last Modified: Tue, 13 Feb 2024 01:53:54 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:98bc5d459492dc920f2634c7d2a39252f464f40045e8ee9bb9a967df561e7fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2155528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741936c96e550374e6be8d4320cd5b8e3cf1b315e382afac934f7edfc2236eb3`

```dockerfile
```

-	Layers:
	-	`sha256:53aa4312033ace4a7cf6f547e9085d8bd6890df5b2615d784fc182399ed92297`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 2.1 MB (2136223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3060f20bd073e1f89280df62e40daa82ac66677706d6628b0e7ce70250402b51`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 19.3 KB (19305 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:42518fad4d8a20363e408d6bf3ce4259a1203bc1f3a1720ede05055daf233cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.3 MB (193349040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc361617127c03f5ef43a89da3fa93390c1213068a6e940b721330dc4e63a12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:b65bdf3d9277efbf6bbf8bf0121f92bdcd342ed0c4f49f1cee3b91adafacd76c in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b1cce6d9947985e4270ac998aa258401bc5deca94d504040a14f9f3c47258d68`  
		Last Modified: Tue, 13 Feb 2024 00:43:56 GMT  
		Size: 33.1 MB (33118908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a48b566372cb4fa0fec129e803c39a28de529b9736fd03a42344641249c1fc`  
		Last Modified: Tue, 13 Feb 2024 21:54:44 GMT  
		Size: 6.2 MB (6239799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85e6dfe440366f653bf664315e491fe0cb2bb189428018fbcf657460fbbc3fa`  
		Last Modified: Tue, 13 Feb 2024 21:54:47 GMT  
		Size: 154.0 MB (153989961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6306b805ea4661e164d23cfd0d8dfae9d27c498477a790d3351d0f6ecc3e5fd`  
		Last Modified: Tue, 13 Feb 2024 21:54:43 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:8ed461f46641215c54d31c67c06954851c85f63b1d2b4eebe9351ecff9289da9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2161862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286b8e56e5b1f465b474b30b2fe8512b0c2238bef520a8bd95c4e5e31b59df2c`

```dockerfile
```

-	Layers:
	-	`sha256:9da0b3fffb06b598b8c17e331a4e70d4e6b54c5bfad5a40d4e88a16d3966ab41`  
		Last Modified: Tue, 13 Feb 2024 21:54:43 GMT  
		Size: 2.1 MB (2142609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbfe360df232fd616240d3f8aae495b7a956d6a7383dcdf4dc8ae56cd7d319c2`  
		Last Modified: Tue, 13 Feb 2024 21:54:43 GMT  
		Size: 19.3 KB (19253 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-bullseye`

```console
$ docker pull julia@sha256:f6dd1793015df42b577c0375b98514ba7979171f5957bb0e475aa3539ef21d5d
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

### `julia:1.10-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:8d384ae00c7c02cbee899728190fcdd1faca693ec80fed6d734c76a84922a118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 MB (204925804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19950a8b05c384b4f92d751f4f10a98e63aa069ead4d5cf9186b030c920da3a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f3f6d4871c74f7b63e34b697a9aaefa8835f1889dc6903866338a86317002e`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 2.4 MB (2426534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba72295cd998aea9729c2a415acf7f007a528c2b4d6f1c34387bb92d9bac746`  
		Last Modified: Tue, 13 Feb 2024 01:53:58 GMT  
		Size: 171.1 MB (171076476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d0425419406b5a1143dff3543f91ff035c7d0ecb9bf0774e64e01554e02e20`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:8273a9fdda9b316a362eeb3ea1e578ee9092b278a30a718754a7c3a8deacd3e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04952d04716e6ab86f7cf6f5e35bd7873721540b5380dd2811279304f811d7f4`

```dockerfile
```

-	Layers:
	-	`sha256:432180086c941804e7ee5fcf6bd251520e95f0fdb359e58e157794fe17baa0b4`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 2.4 MB (2359551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:870a84f47d45ed4bb0321a5cc4914f58d0ee37c40ea0d352c1b840eaa8d48cca`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 18.2 KB (18186 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:5487dbd9e86ea6dfdde1e83477c820ef9096cbd52e19dcc574b6fd9efb76b2ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.9 MB (196864925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80daa6ec8fc78a3eec97067ae5b96e344d99367cccefba598286c51b1386fdf0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1acd381bc5ce074386a44640a70f3d2d53921e7cda7c6386a20616c9fab4cee5`  
		Last Modified: Wed, 14 Feb 2024 00:41:34 GMT  
		Size: 2.4 MB (2415040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520a7f557218cd3b5ef3f4ddd5afcca8d80438c186a9bf2521eda165facd2c91`  
		Last Modified: Wed, 14 Feb 2024 00:41:38 GMT  
		Size: 164.4 MB (164378442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:268a60e13473050784334fa5d0cc23da2209b45f3251f0133c2c05c309d0b752`  
		Last Modified: Wed, 14 Feb 2024 00:41:33 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:f8bb44f08113f3d1137034416ccf2f473631f08424eb97007061de4ac057ae2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2376931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:951d6f2d9e6a3d58bcd7de98a60c4417e42eeafb974b36e71f6fb0760357a357`

```dockerfile
```

-	Layers:
	-	`sha256:7beff45e48bb073460b5214a082784914cd78b5c8864627f675670dff6784190`  
		Last Modified: Wed, 14 Feb 2024 00:41:34 GMT  
		Size: 2.4 MB (2358903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2687ab055e0cc2332a76ad9df388d45043b631992252746a3b6d1260836fc41`  
		Last Modified: Wed, 14 Feb 2024 00:41:34 GMT  
		Size: 18.0 KB (18028 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bullseye` - linux; 386

```console
$ docker pull julia@sha256:3348a4e15f9eb821e27b64f594aee5b549605b9a02ce2d81bf0296660348dccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191411992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34cc23d0f384f592a3f59a3d676eb76d72ea43b54725d5f8e0baeb644aebdffb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:9eaee5af136d095dc1dac0ffce0fde09d8f1bd02ff7cb65ee67e00b2a66f34f7 in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1ac8173b08d16f9f136fb0e3ee39999cef7495f924ecb43f3ca4a4eea267cc88`  
		Last Modified: Tue, 13 Feb 2024 00:44:36 GMT  
		Size: 32.4 MB (32407443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf492369ec4d56d2010213bf0c01a1d0be40c950eda27da51921ed8c2a1bc09`  
		Last Modified: Tue, 13 Feb 2024 01:53:53 GMT  
		Size: 2.5 MB (2533067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7d0f5baeea89d7b49c54cc577eab3867247693f466f98b3cc4f2399efcb0af`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 156.5 MB (156471113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6be2aecc9dc90a8f90619365daf78c2fc8f2c67056592b5b10683e9b84c892`  
		Last Modified: Tue, 13 Feb 2024 01:53:53 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:8016124e8b1742e9b8063df61bae834e255e72ef863ed54fde680195b00a6e09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2374912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9820be04702fdac240a66ebb9fed36ff9a01b291501d69df9966aaa79cbb048`

```dockerfile
```

-	Layers:
	-	`sha256:b5b0fa0ccbf3afd955632b36296386d1988c6a60b808e7101b4b3f9320935cd2`  
		Last Modified: Tue, 13 Feb 2024 01:53:53 GMT  
		Size: 2.4 MB (2356757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:427416a00deb6fc64dea6ac42ea75526fa410b61d0f98ed7c269e848697a670b`  
		Last Modified: Tue, 13 Feb 2024 01:53:53 GMT  
		Size: 18.2 KB (18155 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bullseye` - linux; ppc64le

```console
$ docker pull julia@sha256:34e38bddb83d3e554661ccd943af43cdb864af337b665e80d319d17641dcae38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.9 MB (191918984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce2e008edde3927a13f00754ee8f8a138c1cccfbf871fbecc2c26aa365977fee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:f8e53a63f5fbfb32b4bac66dc2b16f2e2d101e5feb6cd9e3b6d3065fb8aee14d in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5c87ba6a2e42f083a6cfdea0d3b1b3bc977a5065ff0087fdbf4fc8dbc7982a38`  
		Last Modified: Tue, 13 Feb 2024 00:44:50 GMT  
		Size: 35.3 MB (35297799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc406362a4b5aed4760caff7c4bc06a04cb2bd3834a923f056a5baf70eb0d7ff`  
		Last Modified: Tue, 13 Feb 2024 21:56:31 GMT  
		Size: 2.6 MB (2629991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278b4e0551a3587b5d022b566e56d527b968803375aa151bdd2dc6d30b7c7813`  
		Last Modified: Tue, 13 Feb 2024 21:56:34 GMT  
		Size: 154.0 MB (153990822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a158664e796ca3ee0566bb6b7e2b79e13c3161c9f36f6dadb04bf7cdcbb6e58`  
		Last Modified: Tue, 13 Feb 2024 21:56:30 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:074faa55f685aff95e390f40bbece0962016efb2de45e76932ad7ec77379eb75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adae430aa8a2857fe05d29dfd22203f96e4ba41334491bf64c9bcf168e2689ce`

```dockerfile
```

-	Layers:
	-	`sha256:a3834b7b363b094f8ccc42c1d8c1266c29a4d88ab2002bc4a6d745aef0871e7b`  
		Last Modified: Tue, 13 Feb 2024 21:56:30 GMT  
		Size: 2.4 MB (2363081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22fd53c802c699b2d4eec0a68f896ffad71210add2b28509849ee2d177075647`  
		Last Modified: Tue, 13 Feb 2024 21:56:30 GMT  
		Size: 18.1 KB (18059 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-windowsservercore`

```console
$ docker pull julia@sha256:e0173a4d8892b7b6234c3d97cc83366460fefb0737c3333da0fda52b9f2fe0c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `julia:1.10-windowsservercore` - windows version 10.0.20348.2227; amd64

```console
$ docker pull julia@sha256:795c32c108c365c2480a69a195c9a7e377678d314eefe72f64c230c9178355af
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2083272778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe626ae4264c3793e3f2752abc204a549a77a114b9658003d2cda440332150c6`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Thu, 11 Jan 2024 00:02:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:02:52 GMT
ENV JULIA_VERSION=1.10.0
# Thu, 11 Jan 2024 00:02:53 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.0-win64.exe
# Thu, 11 Jan 2024 00:02:54 GMT
ENV JULIA_SHA256=f58aaa631748a5b0389586f3a3b7a081a2a6ac219a5a73a501ac61c0d99daebd
# Thu, 11 Jan 2024 00:04:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:04:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c4a7e196fc6ca93a61a3bbf497fb2b0eca327aa5cf473b95639f61b03c7c1d7`  
		Last Modified: Thu, 11 Jan 2024 00:04:09 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9346ba0550e4beb52f6dad09e1fa6fcd503e75c3df053e5648a54d6dfa7f05`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d7e35a894e972ab63511466519f9a4136a6144e7dbbd6e622be148046ddbaf`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e808d436d368c0aa304f09221c040769d471ae77d9fc07a9bad5a4eff093923`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86dd2e2e2c87845e244df41b72633372b4b9795242f069b3ab2ccbc728756ce8`  
		Last Modified: Thu, 11 Jan 2024 00:04:32 GMT  
		Size: 183.1 MB (183053648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c2cf5808cd6dced23f08a2d0921f88eae3754821b91d2df3decb5d5c8638a6`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10-windowsservercore` - windows version 10.0.17763.5329; amd64

```console
$ docker pull julia@sha256:465739c99dd446c2698ee1f7151fc4f82c353749d9bc6b828a0e5e1db645c233
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2252827649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e690842a775a28bffae7fca39b8fa765ab792fabd7d6883bbc561866e2726e`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:03:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:03:43 GMT
ENV JULIA_VERSION=1.10.0
# Thu, 11 Jan 2024 00:03:44 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.0-win64.exe
# Thu, 11 Jan 2024 00:03:44 GMT
ENV JULIA_SHA256=f58aaa631748a5b0389586f3a3b7a081a2a6ac219a5a73a501ac61c0d99daebd
# Thu, 11 Jan 2024 00:05:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:05:27 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9e301d4f97511dcb9f3216268f983f8b8a38f59f6f47d7fcfa6c74bd89340c`  
		Last Modified: Thu, 11 Jan 2024 00:05:35 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15e9906d04250bd67cb869011a80e67292f17770b36865f9ce3b3f07765278f`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6305ccc6bbbc63d35ea2541315eff9b40ff82631ddc08cf97bae6597d416e35d`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fead423ba6e49e59afeb0485520bcfc1ca1f5231bc0104438c670c75c56d67a`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de60c693e3b77965993cdcd8ccef1ce49bbfd61e59f5e5f85a7b950645ce499b`  
		Last Modified: Thu, 11 Jan 2024 00:05:58 GMT  
		Size: 183.1 MB (183098483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ab8928320d6137aceb0a714f2cc037f1c072f50385773b2f6f1d39368da3fc`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-windowsservercore-1809`

```console
$ docker pull julia@sha256:999bd26e0d2f8bf19acbc55dbda3f7303d67f591de5cfdfe5a04914cc44d8c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `julia:1.10-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull julia@sha256:465739c99dd446c2698ee1f7151fc4f82c353749d9bc6b828a0e5e1db645c233
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2252827649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e690842a775a28bffae7fca39b8fa765ab792fabd7d6883bbc561866e2726e`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:03:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:03:43 GMT
ENV JULIA_VERSION=1.10.0
# Thu, 11 Jan 2024 00:03:44 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.0-win64.exe
# Thu, 11 Jan 2024 00:03:44 GMT
ENV JULIA_SHA256=f58aaa631748a5b0389586f3a3b7a081a2a6ac219a5a73a501ac61c0d99daebd
# Thu, 11 Jan 2024 00:05:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:05:27 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9e301d4f97511dcb9f3216268f983f8b8a38f59f6f47d7fcfa6c74bd89340c`  
		Last Modified: Thu, 11 Jan 2024 00:05:35 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15e9906d04250bd67cb869011a80e67292f17770b36865f9ce3b3f07765278f`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6305ccc6bbbc63d35ea2541315eff9b40ff82631ddc08cf97bae6597d416e35d`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fead423ba6e49e59afeb0485520bcfc1ca1f5231bc0104438c670c75c56d67a`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de60c693e3b77965993cdcd8ccef1ce49bbfd61e59f5e5f85a7b950645ce499b`  
		Last Modified: Thu, 11 Jan 2024 00:05:58 GMT  
		Size: 183.1 MB (183098483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ab8928320d6137aceb0a714f2cc037f1c072f50385773b2f6f1d39368da3fc`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:473983fe5fe55383db5d0d11749bebef8288fe2bc9eb5a72ab3f76b3e6c45d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `julia:1.10-windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull julia@sha256:795c32c108c365c2480a69a195c9a7e377678d314eefe72f64c230c9178355af
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2083272778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe626ae4264c3793e3f2752abc204a549a77a114b9658003d2cda440332150c6`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Thu, 11 Jan 2024 00:02:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:02:52 GMT
ENV JULIA_VERSION=1.10.0
# Thu, 11 Jan 2024 00:02:53 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.0-win64.exe
# Thu, 11 Jan 2024 00:02:54 GMT
ENV JULIA_SHA256=f58aaa631748a5b0389586f3a3b7a081a2a6ac219a5a73a501ac61c0d99daebd
# Thu, 11 Jan 2024 00:04:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:04:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c4a7e196fc6ca93a61a3bbf497fb2b0eca327aa5cf473b95639f61b03c7c1d7`  
		Last Modified: Thu, 11 Jan 2024 00:04:09 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9346ba0550e4beb52f6dad09e1fa6fcd503e75c3df053e5648a54d6dfa7f05`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d7e35a894e972ab63511466519f9a4136a6144e7dbbd6e622be148046ddbaf`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e808d436d368c0aa304f09221c040769d471ae77d9fc07a9bad5a4eff093923`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86dd2e2e2c87845e244df41b72633372b4b9795242f069b3ab2ccbc728756ce8`  
		Last Modified: Thu, 11 Jan 2024 00:04:32 GMT  
		Size: 183.1 MB (183053648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c2cf5808cd6dced23f08a2d0921f88eae3754821b91d2df3decb5d5c8638a6`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.0`

```console
$ docker pull julia@sha256:564460379e4782890dbfe5f073481eceb044b96cefb69f45805f9901fee5a747
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
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `julia:1.10.0` - linux; amd64

```console
$ docker pull julia@sha256:c581649ac221ebfbea9798a3bd66dfb0ba0dd44ba20ff5262d3c8bb93a759346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.9 MB (205909072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b184ca25c5acda81d0dc2e137ccf411bdd8e9f61fdd835d4bd55637d23b835`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad1c4eb009e797d65c1acfac69cd12c8f9060f29f760108f933027f2caab9c3`  
		Last Modified: Tue, 13 Feb 2024 01:53:54 GMT  
		Size: 5.7 MB (5707977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef8b6ee7f7fb149365afb062c086c37b5b314813fc6ec90095b002f5a925f0b`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 171.1 MB (171076635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d82177bdd251b5f04cc2ba1e5fd4efbafdbd4770a176a106cc21f400dbc05a`  
		Last Modified: Tue, 13 Feb 2024 01:53:54 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.0` - unknown; unknown

```console
$ docker pull julia@sha256:3b5ca3771866b183000dca0a20d1bd2cb30d18b3a75d2ff32ac5cacaf423ef41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2158401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1bf8696406f25674e86fbc2d37065b3233c46aeb745f75fb02a0207775ca9a`

```dockerfile
```

-	Layers:
	-	`sha256:0884c94ffa8afd7175e4fdf92aa18f71815867215f0cde964240ba45b4f94154`  
		Last Modified: Tue, 13 Feb 2024 01:53:54 GMT  
		Size: 2.1 MB (2139045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:348b64f895c758148af65a9d8d6cf1581a93e955b08d7c118bee6923d2672bda`  
		Last Modified: Tue, 13 Feb 2024 01:53:54 GMT  
		Size: 19.4 KB (19356 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.0` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:c7b50eb125b7d60c63329a2c13798bc0c6e71611739c313a8ac466b505e9daab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199068374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc9cfd7eb49e87c970aa3df455f5951bd13608a351ad60fa41258f33c872dad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b14e605bd6638a1976eeb8d1cde59556a1f77295bac46d1669a9e27e6cd0ad6`  
		Last Modified: Wed, 14 Feb 2024 00:40:29 GMT  
		Size: 5.5 MB (5533149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d7d4913392d7182590a28188bd4fa882d0ed53f36bf9d49c1b5dfd74dda0ce`  
		Last Modified: Wed, 14 Feb 2024 00:40:32 GMT  
		Size: 164.4 MB (164378492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c05a2fc2483ea3c18ac5829c7ca9c7c9fd40204cb09b4ace74a3c02cb27dbe9`  
		Last Modified: Wed, 14 Feb 2024 00:40:28 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.0` - unknown; unknown

```console
$ docker pull julia@sha256:7812cc45c880626d2dfa14638dfc0dcca6d09a54e1b49abf8d917a8f8a6fd61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2157622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d96f6d9b1c89aaf182d67e03efcae208a6f69ae643a004df4c24d36a84b881f`

```dockerfile
```

-	Layers:
	-	`sha256:ffca818dcaa241a02e65213ba00b90e138a6c248aaa839bb326ddf81d27472f1`  
		Last Modified: Wed, 14 Feb 2024 00:40:29 GMT  
		Size: 2.1 MB (2138415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7b32281e96ad074af12b3d2e1fec978b2b8afb5106ab0eeb89189cedc13c81d`  
		Last Modified: Wed, 14 Feb 2024 00:40:29 GMT  
		Size: 19.2 KB (19207 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.0` - linux; 386

```console
$ docker pull julia@sha256:ed5dae7c246f3779da0892e59fefc8a2a06c1b0418c75cc66df890b64fbd5d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192476013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266a487238b5f50dc9dd3bc262639f4da7f6d7b6194a3f48742cf1725df03675`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adcfe329152d3631bed65ca802c4d591cf2466ececc127b4689e12fd044b6dd9`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 5.9 MB (5863232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7f556d75a67e2c4d02467097026cac3136c670701b05d1fe37c2209b150c66`  
		Last Modified: Tue, 13 Feb 2024 01:53:58 GMT  
		Size: 156.5 MB (156470603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee51a4a243b601cbdaea50eb3df43c6297660d3956259740ebcbb63126d2d0a`  
		Last Modified: Tue, 13 Feb 2024 01:53:54 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.0` - unknown; unknown

```console
$ docker pull julia@sha256:98bc5d459492dc920f2634c7d2a39252f464f40045e8ee9bb9a967df561e7fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2155528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741936c96e550374e6be8d4320cd5b8e3cf1b315e382afac934f7edfc2236eb3`

```dockerfile
```

-	Layers:
	-	`sha256:53aa4312033ace4a7cf6f547e9085d8bd6890df5b2615d784fc182399ed92297`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 2.1 MB (2136223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3060f20bd073e1f89280df62e40daa82ac66677706d6628b0e7ce70250402b51`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 19.3 KB (19305 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.0` - linux; ppc64le

```console
$ docker pull julia@sha256:42518fad4d8a20363e408d6bf3ce4259a1203bc1f3a1720ede05055daf233cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.3 MB (193349040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc361617127c03f5ef43a89da3fa93390c1213068a6e940b721330dc4e63a12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:b65bdf3d9277efbf6bbf8bf0121f92bdcd342ed0c4f49f1cee3b91adafacd76c in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b1cce6d9947985e4270ac998aa258401bc5deca94d504040a14f9f3c47258d68`  
		Last Modified: Tue, 13 Feb 2024 00:43:56 GMT  
		Size: 33.1 MB (33118908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a48b566372cb4fa0fec129e803c39a28de529b9736fd03a42344641249c1fc`  
		Last Modified: Tue, 13 Feb 2024 21:54:44 GMT  
		Size: 6.2 MB (6239799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85e6dfe440366f653bf664315e491fe0cb2bb189428018fbcf657460fbbc3fa`  
		Last Modified: Tue, 13 Feb 2024 21:54:47 GMT  
		Size: 154.0 MB (153989961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6306b805ea4661e164d23cfd0d8dfae9d27c498477a790d3351d0f6ecc3e5fd`  
		Last Modified: Tue, 13 Feb 2024 21:54:43 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.0` - unknown; unknown

```console
$ docker pull julia@sha256:8ed461f46641215c54d31c67c06954851c85f63b1d2b4eebe9351ecff9289da9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2161862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286b8e56e5b1f465b474b30b2fe8512b0c2238bef520a8bd95c4e5e31b59df2c`

```dockerfile
```

-	Layers:
	-	`sha256:9da0b3fffb06b598b8c17e331a4e70d4e6b54c5bfad5a40d4e88a16d3966ab41`  
		Last Modified: Tue, 13 Feb 2024 21:54:43 GMT  
		Size: 2.1 MB (2142609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbfe360df232fd616240d3f8aae495b7a956d6a7383dcdf4dc8ae56cd7d319c2`  
		Last Modified: Tue, 13 Feb 2024 21:54:43 GMT  
		Size: 19.3 KB (19253 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.0` - windows version 10.0.20348.2227; amd64

```console
$ docker pull julia@sha256:795c32c108c365c2480a69a195c9a7e377678d314eefe72f64c230c9178355af
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2083272778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe626ae4264c3793e3f2752abc204a549a77a114b9658003d2cda440332150c6`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Thu, 11 Jan 2024 00:02:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:02:52 GMT
ENV JULIA_VERSION=1.10.0
# Thu, 11 Jan 2024 00:02:53 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.0-win64.exe
# Thu, 11 Jan 2024 00:02:54 GMT
ENV JULIA_SHA256=f58aaa631748a5b0389586f3a3b7a081a2a6ac219a5a73a501ac61c0d99daebd
# Thu, 11 Jan 2024 00:04:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:04:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c4a7e196fc6ca93a61a3bbf497fb2b0eca327aa5cf473b95639f61b03c7c1d7`  
		Last Modified: Thu, 11 Jan 2024 00:04:09 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9346ba0550e4beb52f6dad09e1fa6fcd503e75c3df053e5648a54d6dfa7f05`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d7e35a894e972ab63511466519f9a4136a6144e7dbbd6e622be148046ddbaf`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e808d436d368c0aa304f09221c040769d471ae77d9fc07a9bad5a4eff093923`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86dd2e2e2c87845e244df41b72633372b4b9795242f069b3ab2ccbc728756ce8`  
		Last Modified: Thu, 11 Jan 2024 00:04:32 GMT  
		Size: 183.1 MB (183053648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c2cf5808cd6dced23f08a2d0921f88eae3754821b91d2df3decb5d5c8638a6`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10.0` - windows version 10.0.17763.5329; amd64

```console
$ docker pull julia@sha256:465739c99dd446c2698ee1f7151fc4f82c353749d9bc6b828a0e5e1db645c233
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2252827649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e690842a775a28bffae7fca39b8fa765ab792fabd7d6883bbc561866e2726e`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:03:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:03:43 GMT
ENV JULIA_VERSION=1.10.0
# Thu, 11 Jan 2024 00:03:44 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.0-win64.exe
# Thu, 11 Jan 2024 00:03:44 GMT
ENV JULIA_SHA256=f58aaa631748a5b0389586f3a3b7a081a2a6ac219a5a73a501ac61c0d99daebd
# Thu, 11 Jan 2024 00:05:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:05:27 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9e301d4f97511dcb9f3216268f983f8b8a38f59f6f47d7fcfa6c74bd89340c`  
		Last Modified: Thu, 11 Jan 2024 00:05:35 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15e9906d04250bd67cb869011a80e67292f17770b36865f9ce3b3f07765278f`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6305ccc6bbbc63d35ea2541315eff9b40ff82631ddc08cf97bae6597d416e35d`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fead423ba6e49e59afeb0485520bcfc1ca1f5231bc0104438c670c75c56d67a`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de60c693e3b77965993cdcd8ccef1ce49bbfd61e59f5e5f85a7b950645ce499b`  
		Last Modified: Thu, 11 Jan 2024 00:05:58 GMT  
		Size: 183.1 MB (183098483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ab8928320d6137aceb0a714f2cc037f1c072f50385773b2f6f1d39368da3fc`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.0-alpine`

```console
$ docker pull julia@sha256:15acea4c3855874b1349caf0600c7da2b05033ccfe67d0a8693edf814d1007e8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10.0-alpine` - linux; amd64

```console
$ docker pull julia@sha256:54a01c7689d514bf51a3494279a6877120729ed258de377f503d4782fca53bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176683112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432f75cca29ad8d3247b11295ee97b5a12c070431990e6180904f99400965b39`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["/bin/sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.0-musl-x86_64.tar.gz'; 			sha256='da8a9e0cf31eddd776276321802b9744acf5b8ce0171854b3e9d6394f656f9a2'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d8037af8d1d0f5fa4e82d16f39e0b5b2d7bb3071eeca07feddb80d63a9f084`  
		Last Modified: Sat, 27 Jan 2024 00:53:32 GMT  
		Size: 173.3 MB (173274017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534faee11eeb72a12ad121faf92d04078fb81e27ca029a61603381e7bfdade5c`  
		Last Modified: Sat, 27 Jan 2024 00:53:28 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.0-alpine` - unknown; unknown

```console
$ docker pull julia@sha256:4986f231ec2d9910a78844ccfbbedb86e0c958c6201d42a9a98f2e9208690dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.7 KB (83724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d769d8b51235a19931eb01c03a4bd6662cd2d79ec929b72c3ffd574289061c2a`

```dockerfile
```

-	Layers:
	-	`sha256:ba24d43b9b3ea2e4c533f1d19a970a9e97e8d6fdd95a182466235e35e952196e`  
		Last Modified: Sat, 27 Jan 2024 00:53:28 GMT  
		Size: 69.0 KB (69026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abe1763c27a7fb5692262541e30b12b927086a838ced1e6191ae3bdba7e05191`  
		Last Modified: Sat, 27 Jan 2024 00:53:28 GMT  
		Size: 14.7 KB (14698 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.0-alpine3.18`

```console
$ docker pull julia@sha256:77a977b5edcfe0878250b81503abbe31f1425e64a0f12e1ada4d51b1da34758c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10.0-alpine3.18` - linux; amd64

```console
$ docker pull julia@sha256:5299d783ae55d8ef632b9cc263458d66a810a4de77a03ffae4e7fa820264aa53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176676774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee49bd257b2df90a18d0154e828326a5fcba99b347173d2169fe13bcd43dff0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["/bin/sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.0-musl-x86_64.tar.gz'; 			sha256='da8a9e0cf31eddd776276321802b9744acf5b8ce0171854b3e9d6394f656f9a2'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=alpine&os_version=3.18"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5204fc615595fd1ad835b0750c5fdb927818512d88052aef7e3850c09dd45475`  
		Last Modified: Sat, 27 Jan 2024 00:53:33 GMT  
		Size: 173.3 MB (173273866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3bd7244621863d2bbcbbe233abec587e6b376a86cab3eaec7803f2556e535f`  
		Last Modified: Sat, 27 Jan 2024 00:53:29 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.0-alpine3.18` - unknown; unknown

```console
$ docker pull julia@sha256:da0ca027e598e9773b125a066c844f5cefc1ecbbfb387e5b7661abd53bd31fe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 KB (80746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c093cd0eedbfc6980a82434ffc3879914906fc76b8f084df18d5c9012ffdb2aa`

```dockerfile
```

-	Layers:
	-	`sha256:58ec49d3d0285541a48ea975d3b7fdda895fc33f2c2d93c8933a42c1a3651f1a`  
		Last Modified: Sat, 27 Jan 2024 00:53:29 GMT  
		Size: 67.3 KB (67260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:187a1d23ed3a8d36572659404c674c1615b777fd9041abe5246a10eb10691ae7`  
		Last Modified: Sat, 27 Jan 2024 00:53:29 GMT  
		Size: 13.5 KB (13486 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.0-alpine3.19`

```console
$ docker pull julia@sha256:15acea4c3855874b1349caf0600c7da2b05033ccfe67d0a8693edf814d1007e8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10.0-alpine3.19` - linux; amd64

```console
$ docker pull julia@sha256:54a01c7689d514bf51a3494279a6877120729ed258de377f503d4782fca53bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176683112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432f75cca29ad8d3247b11295ee97b5a12c070431990e6180904f99400965b39`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["/bin/sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.0-musl-x86_64.tar.gz'; 			sha256='da8a9e0cf31eddd776276321802b9744acf5b8ce0171854b3e9d6394f656f9a2'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d8037af8d1d0f5fa4e82d16f39e0b5b2d7bb3071eeca07feddb80d63a9f084`  
		Last Modified: Sat, 27 Jan 2024 00:53:32 GMT  
		Size: 173.3 MB (173274017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534faee11eeb72a12ad121faf92d04078fb81e27ca029a61603381e7bfdade5c`  
		Last Modified: Sat, 27 Jan 2024 00:53:28 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.0-alpine3.19` - unknown; unknown

```console
$ docker pull julia@sha256:4986f231ec2d9910a78844ccfbbedb86e0c958c6201d42a9a98f2e9208690dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.7 KB (83724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d769d8b51235a19931eb01c03a4bd6662cd2d79ec929b72c3ffd574289061c2a`

```dockerfile
```

-	Layers:
	-	`sha256:ba24d43b9b3ea2e4c533f1d19a970a9e97e8d6fdd95a182466235e35e952196e`  
		Last Modified: Sat, 27 Jan 2024 00:53:28 GMT  
		Size: 69.0 KB (69026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abe1763c27a7fb5692262541e30b12b927086a838ced1e6191ae3bdba7e05191`  
		Last Modified: Sat, 27 Jan 2024 00:53:28 GMT  
		Size: 14.7 KB (14698 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.0-bookworm`

```console
$ docker pull julia@sha256:ae0f50e0d812f1537df24444125ca4b894e0e4a0e293b897b9ada6726f0ac007
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

### `julia:1.10.0-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:c581649ac221ebfbea9798a3bd66dfb0ba0dd44ba20ff5262d3c8bb93a759346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.9 MB (205909072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b184ca25c5acda81d0dc2e137ccf411bdd8e9f61fdd835d4bd55637d23b835`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad1c4eb009e797d65c1acfac69cd12c8f9060f29f760108f933027f2caab9c3`  
		Last Modified: Tue, 13 Feb 2024 01:53:54 GMT  
		Size: 5.7 MB (5707977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef8b6ee7f7fb149365afb062c086c37b5b314813fc6ec90095b002f5a925f0b`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 171.1 MB (171076635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d82177bdd251b5f04cc2ba1e5fd4efbafdbd4770a176a106cc21f400dbc05a`  
		Last Modified: Tue, 13 Feb 2024 01:53:54 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.0-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:3b5ca3771866b183000dca0a20d1bd2cb30d18b3a75d2ff32ac5cacaf423ef41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2158401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1bf8696406f25674e86fbc2d37065b3233c46aeb745f75fb02a0207775ca9a`

```dockerfile
```

-	Layers:
	-	`sha256:0884c94ffa8afd7175e4fdf92aa18f71815867215f0cde964240ba45b4f94154`  
		Last Modified: Tue, 13 Feb 2024 01:53:54 GMT  
		Size: 2.1 MB (2139045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:348b64f895c758148af65a9d8d6cf1581a93e955b08d7c118bee6923d2672bda`  
		Last Modified: Tue, 13 Feb 2024 01:53:54 GMT  
		Size: 19.4 KB (19356 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:c7b50eb125b7d60c63329a2c13798bc0c6e71611739c313a8ac466b505e9daab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199068374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc9cfd7eb49e87c970aa3df455f5951bd13608a351ad60fa41258f33c872dad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b14e605bd6638a1976eeb8d1cde59556a1f77295bac46d1669a9e27e6cd0ad6`  
		Last Modified: Wed, 14 Feb 2024 00:40:29 GMT  
		Size: 5.5 MB (5533149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d7d4913392d7182590a28188bd4fa882d0ed53f36bf9d49c1b5dfd74dda0ce`  
		Last Modified: Wed, 14 Feb 2024 00:40:32 GMT  
		Size: 164.4 MB (164378492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c05a2fc2483ea3c18ac5829c7ca9c7c9fd40204cb09b4ace74a3c02cb27dbe9`  
		Last Modified: Wed, 14 Feb 2024 00:40:28 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.0-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:7812cc45c880626d2dfa14638dfc0dcca6d09a54e1b49abf8d917a8f8a6fd61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2157622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d96f6d9b1c89aaf182d67e03efcae208a6f69ae643a004df4c24d36a84b881f`

```dockerfile
```

-	Layers:
	-	`sha256:ffca818dcaa241a02e65213ba00b90e138a6c248aaa839bb326ddf81d27472f1`  
		Last Modified: Wed, 14 Feb 2024 00:40:29 GMT  
		Size: 2.1 MB (2138415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7b32281e96ad074af12b3d2e1fec978b2b8afb5106ab0eeb89189cedc13c81d`  
		Last Modified: Wed, 14 Feb 2024 00:40:29 GMT  
		Size: 19.2 KB (19207 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.0-bookworm` - linux; 386

```console
$ docker pull julia@sha256:ed5dae7c246f3779da0892e59fefc8a2a06c1b0418c75cc66df890b64fbd5d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192476013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266a487238b5f50dc9dd3bc262639f4da7f6d7b6194a3f48742cf1725df03675`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adcfe329152d3631bed65ca802c4d591cf2466ececc127b4689e12fd044b6dd9`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 5.9 MB (5863232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7f556d75a67e2c4d02467097026cac3136c670701b05d1fe37c2209b150c66`  
		Last Modified: Tue, 13 Feb 2024 01:53:58 GMT  
		Size: 156.5 MB (156470603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee51a4a243b601cbdaea50eb3df43c6297660d3956259740ebcbb63126d2d0a`  
		Last Modified: Tue, 13 Feb 2024 01:53:54 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.0-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:98bc5d459492dc920f2634c7d2a39252f464f40045e8ee9bb9a967df561e7fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2155528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741936c96e550374e6be8d4320cd5b8e3cf1b315e382afac934f7edfc2236eb3`

```dockerfile
```

-	Layers:
	-	`sha256:53aa4312033ace4a7cf6f547e9085d8bd6890df5b2615d784fc182399ed92297`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 2.1 MB (2136223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3060f20bd073e1f89280df62e40daa82ac66677706d6628b0e7ce70250402b51`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 19.3 KB (19305 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.0-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:42518fad4d8a20363e408d6bf3ce4259a1203bc1f3a1720ede05055daf233cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.3 MB (193349040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc361617127c03f5ef43a89da3fa93390c1213068a6e940b721330dc4e63a12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:b65bdf3d9277efbf6bbf8bf0121f92bdcd342ed0c4f49f1cee3b91adafacd76c in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b1cce6d9947985e4270ac998aa258401bc5deca94d504040a14f9f3c47258d68`  
		Last Modified: Tue, 13 Feb 2024 00:43:56 GMT  
		Size: 33.1 MB (33118908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a48b566372cb4fa0fec129e803c39a28de529b9736fd03a42344641249c1fc`  
		Last Modified: Tue, 13 Feb 2024 21:54:44 GMT  
		Size: 6.2 MB (6239799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85e6dfe440366f653bf664315e491fe0cb2bb189428018fbcf657460fbbc3fa`  
		Last Modified: Tue, 13 Feb 2024 21:54:47 GMT  
		Size: 154.0 MB (153989961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6306b805ea4661e164d23cfd0d8dfae9d27c498477a790d3351d0f6ecc3e5fd`  
		Last Modified: Tue, 13 Feb 2024 21:54:43 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.0-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:8ed461f46641215c54d31c67c06954851c85f63b1d2b4eebe9351ecff9289da9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2161862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286b8e56e5b1f465b474b30b2fe8512b0c2238bef520a8bd95c4e5e31b59df2c`

```dockerfile
```

-	Layers:
	-	`sha256:9da0b3fffb06b598b8c17e331a4e70d4e6b54c5bfad5a40d4e88a16d3966ab41`  
		Last Modified: Tue, 13 Feb 2024 21:54:43 GMT  
		Size: 2.1 MB (2142609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbfe360df232fd616240d3f8aae495b7a956d6a7383dcdf4dc8ae56cd7d319c2`  
		Last Modified: Tue, 13 Feb 2024 21:54:43 GMT  
		Size: 19.3 KB (19253 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.0-bullseye`

```console
$ docker pull julia@sha256:f6dd1793015df42b577c0375b98514ba7979171f5957bb0e475aa3539ef21d5d
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

### `julia:1.10.0-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:8d384ae00c7c02cbee899728190fcdd1faca693ec80fed6d734c76a84922a118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 MB (204925804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19950a8b05c384b4f92d751f4f10a98e63aa069ead4d5cf9186b030c920da3a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f3f6d4871c74f7b63e34b697a9aaefa8835f1889dc6903866338a86317002e`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 2.4 MB (2426534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba72295cd998aea9729c2a415acf7f007a528c2b4d6f1c34387bb92d9bac746`  
		Last Modified: Tue, 13 Feb 2024 01:53:58 GMT  
		Size: 171.1 MB (171076476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d0425419406b5a1143dff3543f91ff035c7d0ecb9bf0774e64e01554e02e20`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.0-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:8273a9fdda9b316a362eeb3ea1e578ee9092b278a30a718754a7c3a8deacd3e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04952d04716e6ab86f7cf6f5e35bd7873721540b5380dd2811279304f811d7f4`

```dockerfile
```

-	Layers:
	-	`sha256:432180086c941804e7ee5fcf6bd251520e95f0fdb359e58e157794fe17baa0b4`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 2.4 MB (2359551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:870a84f47d45ed4bb0321a5cc4914f58d0ee37c40ea0d352c1b840eaa8d48cca`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 18.2 KB (18186 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:5487dbd9e86ea6dfdde1e83477c820ef9096cbd52e19dcc574b6fd9efb76b2ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.9 MB (196864925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80daa6ec8fc78a3eec97067ae5b96e344d99367cccefba598286c51b1386fdf0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1acd381bc5ce074386a44640a70f3d2d53921e7cda7c6386a20616c9fab4cee5`  
		Last Modified: Wed, 14 Feb 2024 00:41:34 GMT  
		Size: 2.4 MB (2415040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520a7f557218cd3b5ef3f4ddd5afcca8d80438c186a9bf2521eda165facd2c91`  
		Last Modified: Wed, 14 Feb 2024 00:41:38 GMT  
		Size: 164.4 MB (164378442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:268a60e13473050784334fa5d0cc23da2209b45f3251f0133c2c05c309d0b752`  
		Last Modified: Wed, 14 Feb 2024 00:41:33 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.0-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:f8bb44f08113f3d1137034416ccf2f473631f08424eb97007061de4ac057ae2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2376931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:951d6f2d9e6a3d58bcd7de98a60c4417e42eeafb974b36e71f6fb0760357a357`

```dockerfile
```

-	Layers:
	-	`sha256:7beff45e48bb073460b5214a082784914cd78b5c8864627f675670dff6784190`  
		Last Modified: Wed, 14 Feb 2024 00:41:34 GMT  
		Size: 2.4 MB (2358903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2687ab055e0cc2332a76ad9df388d45043b631992252746a3b6d1260836fc41`  
		Last Modified: Wed, 14 Feb 2024 00:41:34 GMT  
		Size: 18.0 KB (18028 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.0-bullseye` - linux; 386

```console
$ docker pull julia@sha256:3348a4e15f9eb821e27b64f594aee5b549605b9a02ce2d81bf0296660348dccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191411992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34cc23d0f384f592a3f59a3d676eb76d72ea43b54725d5f8e0baeb644aebdffb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:9eaee5af136d095dc1dac0ffce0fde09d8f1bd02ff7cb65ee67e00b2a66f34f7 in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1ac8173b08d16f9f136fb0e3ee39999cef7495f924ecb43f3ca4a4eea267cc88`  
		Last Modified: Tue, 13 Feb 2024 00:44:36 GMT  
		Size: 32.4 MB (32407443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf492369ec4d56d2010213bf0c01a1d0be40c950eda27da51921ed8c2a1bc09`  
		Last Modified: Tue, 13 Feb 2024 01:53:53 GMT  
		Size: 2.5 MB (2533067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7d0f5baeea89d7b49c54cc577eab3867247693f466f98b3cc4f2399efcb0af`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 156.5 MB (156471113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6be2aecc9dc90a8f90619365daf78c2fc8f2c67056592b5b10683e9b84c892`  
		Last Modified: Tue, 13 Feb 2024 01:53:53 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.0-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:8016124e8b1742e9b8063df61bae834e255e72ef863ed54fde680195b00a6e09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2374912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9820be04702fdac240a66ebb9fed36ff9a01b291501d69df9966aaa79cbb048`

```dockerfile
```

-	Layers:
	-	`sha256:b5b0fa0ccbf3afd955632b36296386d1988c6a60b808e7101b4b3f9320935cd2`  
		Last Modified: Tue, 13 Feb 2024 01:53:53 GMT  
		Size: 2.4 MB (2356757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:427416a00deb6fc64dea6ac42ea75526fa410b61d0f98ed7c269e848697a670b`  
		Last Modified: Tue, 13 Feb 2024 01:53:53 GMT  
		Size: 18.2 KB (18155 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.0-bullseye` - linux; ppc64le

```console
$ docker pull julia@sha256:34e38bddb83d3e554661ccd943af43cdb864af337b665e80d319d17641dcae38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.9 MB (191918984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce2e008edde3927a13f00754ee8f8a138c1cccfbf871fbecc2c26aa365977fee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:f8e53a63f5fbfb32b4bac66dc2b16f2e2d101e5feb6cd9e3b6d3065fb8aee14d in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5c87ba6a2e42f083a6cfdea0d3b1b3bc977a5065ff0087fdbf4fc8dbc7982a38`  
		Last Modified: Tue, 13 Feb 2024 00:44:50 GMT  
		Size: 35.3 MB (35297799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc406362a4b5aed4760caff7c4bc06a04cb2bd3834a923f056a5baf70eb0d7ff`  
		Last Modified: Tue, 13 Feb 2024 21:56:31 GMT  
		Size: 2.6 MB (2629991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278b4e0551a3587b5d022b566e56d527b968803375aa151bdd2dc6d30b7c7813`  
		Last Modified: Tue, 13 Feb 2024 21:56:34 GMT  
		Size: 154.0 MB (153990822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a158664e796ca3ee0566bb6b7e2b79e13c3161c9f36f6dadb04bf7cdcbb6e58`  
		Last Modified: Tue, 13 Feb 2024 21:56:30 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.0-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:074faa55f685aff95e390f40bbece0962016efb2de45e76932ad7ec77379eb75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adae430aa8a2857fe05d29dfd22203f96e4ba41334491bf64c9bcf168e2689ce`

```dockerfile
```

-	Layers:
	-	`sha256:a3834b7b363b094f8ccc42c1d8c1266c29a4d88ab2002bc4a6d745aef0871e7b`  
		Last Modified: Tue, 13 Feb 2024 21:56:30 GMT  
		Size: 2.4 MB (2363081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22fd53c802c699b2d4eec0a68f896ffad71210add2b28509849ee2d177075647`  
		Last Modified: Tue, 13 Feb 2024 21:56:30 GMT  
		Size: 18.1 KB (18059 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.0-windowsservercore`

```console
$ docker pull julia@sha256:e0173a4d8892b7b6234c3d97cc83366460fefb0737c3333da0fda52b9f2fe0c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `julia:1.10.0-windowsservercore` - windows version 10.0.20348.2227; amd64

```console
$ docker pull julia@sha256:795c32c108c365c2480a69a195c9a7e377678d314eefe72f64c230c9178355af
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2083272778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe626ae4264c3793e3f2752abc204a549a77a114b9658003d2cda440332150c6`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Thu, 11 Jan 2024 00:02:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:02:52 GMT
ENV JULIA_VERSION=1.10.0
# Thu, 11 Jan 2024 00:02:53 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.0-win64.exe
# Thu, 11 Jan 2024 00:02:54 GMT
ENV JULIA_SHA256=f58aaa631748a5b0389586f3a3b7a081a2a6ac219a5a73a501ac61c0d99daebd
# Thu, 11 Jan 2024 00:04:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:04:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c4a7e196fc6ca93a61a3bbf497fb2b0eca327aa5cf473b95639f61b03c7c1d7`  
		Last Modified: Thu, 11 Jan 2024 00:04:09 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9346ba0550e4beb52f6dad09e1fa6fcd503e75c3df053e5648a54d6dfa7f05`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d7e35a894e972ab63511466519f9a4136a6144e7dbbd6e622be148046ddbaf`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e808d436d368c0aa304f09221c040769d471ae77d9fc07a9bad5a4eff093923`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86dd2e2e2c87845e244df41b72633372b4b9795242f069b3ab2ccbc728756ce8`  
		Last Modified: Thu, 11 Jan 2024 00:04:32 GMT  
		Size: 183.1 MB (183053648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c2cf5808cd6dced23f08a2d0921f88eae3754821b91d2df3decb5d5c8638a6`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10.0-windowsservercore` - windows version 10.0.17763.5329; amd64

```console
$ docker pull julia@sha256:465739c99dd446c2698ee1f7151fc4f82c353749d9bc6b828a0e5e1db645c233
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2252827649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e690842a775a28bffae7fca39b8fa765ab792fabd7d6883bbc561866e2726e`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:03:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:03:43 GMT
ENV JULIA_VERSION=1.10.0
# Thu, 11 Jan 2024 00:03:44 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.0-win64.exe
# Thu, 11 Jan 2024 00:03:44 GMT
ENV JULIA_SHA256=f58aaa631748a5b0389586f3a3b7a081a2a6ac219a5a73a501ac61c0d99daebd
# Thu, 11 Jan 2024 00:05:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:05:27 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9e301d4f97511dcb9f3216268f983f8b8a38f59f6f47d7fcfa6c74bd89340c`  
		Last Modified: Thu, 11 Jan 2024 00:05:35 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15e9906d04250bd67cb869011a80e67292f17770b36865f9ce3b3f07765278f`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6305ccc6bbbc63d35ea2541315eff9b40ff82631ddc08cf97bae6597d416e35d`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fead423ba6e49e59afeb0485520bcfc1ca1f5231bc0104438c670c75c56d67a`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de60c693e3b77965993cdcd8ccef1ce49bbfd61e59f5e5f85a7b950645ce499b`  
		Last Modified: Thu, 11 Jan 2024 00:05:58 GMT  
		Size: 183.1 MB (183098483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ab8928320d6137aceb0a714f2cc037f1c072f50385773b2f6f1d39368da3fc`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.0-windowsservercore-1809`

```console
$ docker pull julia@sha256:999bd26e0d2f8bf19acbc55dbda3f7303d67f591de5cfdfe5a04914cc44d8c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `julia:1.10.0-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull julia@sha256:465739c99dd446c2698ee1f7151fc4f82c353749d9bc6b828a0e5e1db645c233
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2252827649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e690842a775a28bffae7fca39b8fa765ab792fabd7d6883bbc561866e2726e`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:03:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:03:43 GMT
ENV JULIA_VERSION=1.10.0
# Thu, 11 Jan 2024 00:03:44 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.0-win64.exe
# Thu, 11 Jan 2024 00:03:44 GMT
ENV JULIA_SHA256=f58aaa631748a5b0389586f3a3b7a081a2a6ac219a5a73a501ac61c0d99daebd
# Thu, 11 Jan 2024 00:05:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:05:27 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9e301d4f97511dcb9f3216268f983f8b8a38f59f6f47d7fcfa6c74bd89340c`  
		Last Modified: Thu, 11 Jan 2024 00:05:35 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15e9906d04250bd67cb869011a80e67292f17770b36865f9ce3b3f07765278f`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6305ccc6bbbc63d35ea2541315eff9b40ff82631ddc08cf97bae6597d416e35d`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fead423ba6e49e59afeb0485520bcfc1ca1f5231bc0104438c670c75c56d67a`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de60c693e3b77965993cdcd8ccef1ce49bbfd61e59f5e5f85a7b950645ce499b`  
		Last Modified: Thu, 11 Jan 2024 00:05:58 GMT  
		Size: 183.1 MB (183098483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ab8928320d6137aceb0a714f2cc037f1c072f50385773b2f6f1d39368da3fc`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.0-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:473983fe5fe55383db5d0d11749bebef8288fe2bc9eb5a72ab3f76b3e6c45d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `julia:1.10.0-windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull julia@sha256:795c32c108c365c2480a69a195c9a7e377678d314eefe72f64c230c9178355af
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2083272778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe626ae4264c3793e3f2752abc204a549a77a114b9658003d2cda440332150c6`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Thu, 11 Jan 2024 00:02:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:02:52 GMT
ENV JULIA_VERSION=1.10.0
# Thu, 11 Jan 2024 00:02:53 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.0-win64.exe
# Thu, 11 Jan 2024 00:02:54 GMT
ENV JULIA_SHA256=f58aaa631748a5b0389586f3a3b7a081a2a6ac219a5a73a501ac61c0d99daebd
# Thu, 11 Jan 2024 00:04:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:04:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c4a7e196fc6ca93a61a3bbf497fb2b0eca327aa5cf473b95639f61b03c7c1d7`  
		Last Modified: Thu, 11 Jan 2024 00:04:09 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9346ba0550e4beb52f6dad09e1fa6fcd503e75c3df053e5648a54d6dfa7f05`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d7e35a894e972ab63511466519f9a4136a6144e7dbbd6e622be148046ddbaf`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e808d436d368c0aa304f09221c040769d471ae77d9fc07a9bad5a4eff093923`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86dd2e2e2c87845e244df41b72633372b4b9795242f069b3ab2ccbc728756ce8`  
		Last Modified: Thu, 11 Jan 2024 00:04:32 GMT  
		Size: 183.1 MB (183053648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c2cf5808cd6dced23f08a2d0921f88eae3754821b91d2df3decb5d5c8638a6`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6`

```console
$ docker pull julia@sha256:d68eedb4de05d8840076683de1e4abe751a4b4d0c67c02c0127f99605a937a41
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `julia:1.6` - linux; amd64

```console
$ docker pull julia@sha256:1e9c9aa0fa242fb4b3a7fb6f67d212a104a2b646edc398128371df8cfe271e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.3 MB (157256279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52873e5ddddf1bd9c9acd2701a47c05e87cb3abe5611c66e947122d2cc09b9bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 10 Nov 2023 15:26:46 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["bash"]
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 10 Nov 2023 15:26:46 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_VERSION=1.6.7
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.6.7","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.6.7?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbdf56e13c93bec7604b443c61718b2b2a556d76f9b2b9d51164899250e09069`  
		Last Modified: Tue, 13 Feb 2024 01:53:46 GMT  
		Size: 5.7 MB (5707962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697dbd1cfee9c43d7f4b9763a6c332d5a0505ad0d54e29efd9e62b49b23b9c33`  
		Last Modified: Tue, 13 Feb 2024 01:53:48 GMT  
		Size: 122.4 MB (122423862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c54cf712f8283756f4fa342c9e3577ce4cfcb42f0975fc7b1b9c7e5e7043e6`  
		Last Modified: Tue, 13 Feb 2024 01:53:46 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.6` - unknown; unknown

```console
$ docker pull julia@sha256:df9cb8c425d0f409537a377661e2d514e16748f8eca85f1c98cfb7b839217d45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2133576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2f0a6c822c077b461b1b0aa885073889a6b7078ca912e3da6faee11e011d40`

```dockerfile
```

-	Layers:
	-	`sha256:14720befa9fad15710243ce7eaf791a52abf6ba5ae772e45b518b78140d4e385`  
		Last Modified: Tue, 13 Feb 2024 01:53:46 GMT  
		Size: 2.1 MB (2115456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89725b6fcddd4182ef8fb630912e0a1c3d5f2992cb869ef2eaf259437c7c75c2`  
		Last Modified: Tue, 13 Feb 2024 01:53:46 GMT  
		Size: 18.1 KB (18120 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.6` - linux; arm variant v7

```console
$ docker pull julia@sha256:35e94e8db589a16b8ddfad20270179bf4dec5fba02f6c83c02f3eaa9cf587e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142847407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b0f754906fefef55f2be2902877bac1776e86f927760a9360761a644c8848f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 10 Nov 2023 15:26:46 GMT
ADD file:d6072ced9736ca566086eea2514cf12faccec9859bbd93e83950ad51f6827e8c in / 
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["bash"]
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 10 Nov 2023 15:26:46 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_VERSION=1.6.7
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.6.7","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.6.7?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:404006a0fd99beed6ef1a9502692bd5005ae8c3b9d36a9b48654f7dfaacfb2c5`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 24.7 MB (24741565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c1ff3c5af224419230c243f5e6ed677cbc45ce6989c3d02bb48009914ff039`  
		Last Modified: Sat, 03 Feb 2024 11:33:25 GMT  
		Size: 4.6 MB (4632669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75bee3d1565fcf900a80fcdf2213b4ae67c4d862f29b584b60f80d7d448fb02`  
		Last Modified: Sat, 03 Feb 2024 11:33:28 GMT  
		Size: 113.5 MB (113472799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60106ec0de297b8ce826f05530ce5fbc7eaaa253a1620c3a79403b6e0c9c64ac`  
		Last Modified: Sat, 03 Feb 2024 11:33:24 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.6` - unknown; unknown

```console
$ docker pull julia@sha256:9de087a177e288c87696be457794ac43b526a03676f70dadf572d901c7924c50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:859525c46727f8495f9e894f5efe5182f220d71ee2dbdb90745e72624f6a8067`

```dockerfile
```

-	Layers:
	-	`sha256:c98f5c67982985c4ff6851cec3dc6551bf3b3e0389d2949a0f20a6038c014989`  
		Last Modified: Sat, 03 Feb 2024 11:33:25 GMT  
		Size: 2.1 MB (2117788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1a3c9f6334d0291d9164ed89ec6e61e2a177792327bbbc99868cac176cbb4d1`  
		Last Modified: Sat, 03 Feb 2024 11:33:24 GMT  
		Size: 18.0 KB (18035 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.6` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:512b438acf54e6bcd1834955126f91210011cabeb171730d33368e7ef49d6a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150901838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aeac16aeed7ef952e0ecd3dc455f2b54fb6cfef91ec778b71e233d4f7ed2321`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 10 Nov 2023 15:26:46 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["bash"]
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 10 Nov 2023 15:26:46 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_VERSION=1.6.7
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.6.7","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.6.7?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b14e605bd6638a1976eeb8d1cde59556a1f77295bac46d1669a9e27e6cd0ad6`  
		Last Modified: Wed, 14 Feb 2024 00:40:29 GMT  
		Size: 5.5 MB (5533149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebde71b115cbf7bafbe0d4417955686065606fe2fa767fc6ed31d12ae4926ba4`  
		Last Modified: Wed, 14 Feb 2024 00:42:29 GMT  
		Size: 116.2 MB (116211958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9451bb0011bcbf1daf2d00410a734f9750c021ad8aebe4d391a64fdb3e1971d1`  
		Last Modified: Wed, 14 Feb 2024 00:42:26 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.6` - unknown; unknown

```console
$ docker pull julia@sha256:8cc763722290d52ec2b1a7fa18c628d2630411b0bbe1a661cac3fb2ec2bb4151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2133754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77fa3a8b17893a35d1023aa52f8adc2684a373d93191eb7ca6260843a1a6b170`

```dockerfile
```

-	Layers:
	-	`sha256:63a9b0ef4a753f8b9fb3fd2346a01b6aa5480cd222052744cf4b000957a1a1b9`  
		Last Modified: Wed, 14 Feb 2024 00:42:26 GMT  
		Size: 2.1 MB (2115791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6f7b5d56798cccc7af9f29454a32b0ef2b633c7c8e51e585db5877186617942`  
		Last Modified: Wed, 14 Feb 2024 00:42:26 GMT  
		Size: 18.0 KB (17963 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.6` - linux; 386

```console
$ docker pull julia@sha256:33f51106daf2cb9f30fe8d9b9062b7b5f81ee6077ce736da915ca0d0310fb9de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156096437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85a982556a5c23ceeb73b8cbf696d3d6a06acc7aa74109a3eae1a627756648e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 10 Nov 2023 15:26:46 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["bash"]
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 10 Nov 2023 15:26:46 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_VERSION=1.6.7
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.6.7","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.6.7?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f077852809d3df0ff0aaa7a7999f678d46ef0610856b3cdfeb43cfa4f5640b9`  
		Last Modified: Tue, 13 Feb 2024 01:53:50 GMT  
		Size: 5.9 MB (5863266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1f1076a2abdc9cee969fb84b5be03f8fa38280081598bd24a7d3571754d0e8`  
		Last Modified: Tue, 13 Feb 2024 01:53:53 GMT  
		Size: 120.1 MB (120090994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8cc012aa6af202e8c794bdeefa180135dd62b2d847c2de62028bb0d8f7d3ec`  
		Last Modified: Tue, 13 Feb 2024 01:53:50 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.6` - unknown; unknown

```console
$ docker pull julia@sha256:591fbb52b8d270de8a94e59e0b76349486c19676866f93ac08fcbc0723755ff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2130741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9492628cf08b5352cfb403a015a7c43586f5f454e1457e5e00619820fed796b4`

```dockerfile
```

-	Layers:
	-	`sha256:a838468fc0caa024ea0293c369b3c4b3704212fd01d445d6e48389a9fae99d63`  
		Last Modified: Tue, 13 Feb 2024 01:53:50 GMT  
		Size: 2.1 MB (2112654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:195d2faeee1d99524485898b2275f5c342519a2088c7821a5981b3aa95aff7cf`  
		Last Modified: Tue, 13 Feb 2024 01:53:50 GMT  
		Size: 18.1 KB (18087 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.6` - windows version 10.0.20348.2227; amd64

```console
$ docker pull julia@sha256:aacbbc8940601c0e5596931fa9d41cce28ab1fa2c31c78c1d116e219483534c7
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2034764054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:543f707ae687e7e690271d7fe6f8b11b7c62dc6f786e23fee7dadc2b52c6351e`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Thu, 11 Jan 2024 00:08:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:08:01 GMT
ENV JULIA_VERSION=1.6.7
# Thu, 11 Jan 2024 00:08:02 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Thu, 11 Jan 2024 00:08:02 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Thu, 11 Jan 2024 00:08:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:08:50 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ec27c9842b8e899a5278c55aa21d2cf14e62ae5b8dbc8ef21ffe38683f694d`  
		Last Modified: Thu, 11 Jan 2024 00:08:56 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12f858d296dd90c13c42516bcc60fae65f52207d2846a54ad3e3c059b87bf85`  
		Last Modified: Thu, 11 Jan 2024 00:08:54 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37065f76f4d697c310167b0cf169601492542ffeb7174129d6077ec8af74ff49`  
		Last Modified: Thu, 11 Jan 2024 00:08:54 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b334853e6c04835809903c081d10c7faa8ee0d9d6d3684d89e8d6954e2725c5`  
		Last Modified: Thu, 11 Jan 2024 00:08:54 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109a7946e539e9a6238d5492f541cd7ce6b55b428fdf1d34f9ead65ac74bb682`  
		Last Modified: Thu, 11 Jan 2024 00:09:12 GMT  
		Size: 134.5 MB (134544929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35917c15fff017c85a175e4c462c3fc80c624510736cf63a746358851e462b7f`  
		Last Modified: Thu, 11 Jan 2024 00:08:54 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6` - windows version 10.0.17763.5329; amd64

```console
$ docker pull julia@sha256:09f0a64aa6af42e12b9c0667122016bbda84151ebbc217b59fc24aa875e3e953
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2204271920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2770e04b2d617a0710f509eaa78ee9e3db8e0c4742f63c90e174a5277fb3889`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:04:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:04:59 GMT
ENV JULIA_VERSION=1.6.7
# Thu, 11 Jan 2024 00:05:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Thu, 11 Jan 2024 00:05:01 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Thu, 11 Jan 2024 00:06:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:06:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018567616bba50c617270b645f6f9f5eeffc82add802ee321a43b1cbcabf047d`  
		Last Modified: Thu, 11 Jan 2024 00:06:29 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f16287f2b89a420c3c6ff9e6b119a9bac0bca4711c2c38160c6725a076af14a`  
		Last Modified: Thu, 11 Jan 2024 00:06:27 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b9460df90a5ea657a924cb2e8e06f9d231da0255adfe2727c85142c3b9acbff`  
		Last Modified: Thu, 11 Jan 2024 00:06:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2307766466bf7a0f3659aed4269cb3895dde01f7f7d2eb6bf4a40a5893ac05b`  
		Last Modified: Thu, 11 Jan 2024 00:06:27 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaceb21bd3ac6440c397b6e7b9de7788c1019a0f1ed396375f20819fb2e82d1`  
		Last Modified: Thu, 11 Jan 2024 00:06:45 GMT  
		Size: 134.5 MB (134542902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4ebe971903a073c38f33636a0c5c3435c9abef3f9e10437c9b35e51c33e674`  
		Last Modified: Thu, 11 Jan 2024 00:06:27 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6-alpine`

```console
$ docker pull julia@sha256:634e2b295d1a176d57a87bf6ad3916546ad9b36922aed24f39d20ac3df909847
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.6-alpine` - linux; amd64

```console
$ docker pull julia@sha256:e2eab0dc4aed438d27d8e47e2b82c6d73e1a9f9736f59d3a0c051c9de65b32f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125238430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a0efb053006ce1a2c3acfb4e228edffc8c81dae4084f828a702d3ae3ae97e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 09 Dec 2023 15:29:30 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 09 Dec 2023 15:29:30 GMT
CMD ["/bin/sh"]
# Sat, 09 Dec 2023 15:29:30 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 09 Dec 2023 15:29:30 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Dec 2023 15:29:30 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 09 Dec 2023 15:29:30 GMT
ENV JULIA_VERSION=1.6.7
# Sat, 09 Dec 2023 15:29:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.6/julia-1.6.7-musl-x86_64.tar.gz'; 			sha256='d71ccc5aa36cf691616a40bf6fb960fac5620ce53d2f90a95947b90dec509433'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.6.7","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.6.7?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Sat, 09 Dec 2023 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 09 Dec 2023 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 09 Dec 2023 15:29:30 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69e0de20d2a2b103d3b92574c30d8e9edbfd15063f4dc3067ca122c50f83b9e`  
		Last Modified: Sat, 27 Jan 2024 00:53:09 GMT  
		Size: 121.8 MB (121829335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52371be8dc23f0d60deb16f0ec1425dc62e573d5c39394fa1fb31e5e19cc21a0`  
		Last Modified: Sat, 27 Jan 2024 00:53:08 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.6-alpine` - unknown; unknown

```console
$ docker pull julia@sha256:da13ca697ea7277d0b9c37e966074fffb314bc6f390ed83340fb4860b72d9287
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.3 KB (80300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bb702dac0ec1518fe072dec676ce70592eca8bef920b99ee3f79258cd15e20b`

```dockerfile
```

-	Layers:
	-	`sha256:61d23b6ea854fd54b94ca4cfa3c6c7033477f5f84165bb6f79e813b6360b5c16`  
		Last Modified: Sat, 27 Jan 2024 00:53:07 GMT  
		Size: 66.8 KB (66835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79f4dfe8c80354d2b8d2ea8a77d7a83f446322f3be7afe42462a8cbbe70df78e`  
		Last Modified: Sat, 27 Jan 2024 00:53:07 GMT  
		Size: 13.5 KB (13465 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.6-alpine3.18`

```console
$ docker pull julia@sha256:9d3f8d87a4169fd0f722e0f6799c5c774430afd56bb76effc51caa08077dba7a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.6-alpine3.18` - linux; amd64

```console
$ docker pull julia@sha256:1db84d51d1be7d36c0e54a8d4ef980f1ad0a5085ce909cf9a3e81fe82db5e4ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125232446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:614e6c7c70e8ac5b7e4711d99c6555a9af8e9b80d5dfc7a27472b7a471b14f7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 10 Nov 2023 15:26:46 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["/bin/sh"]
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 10 Nov 2023 15:26:46 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_VERSION=1.6.7
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.6/julia-1.6.7-musl-x86_64.tar.gz'; 			sha256='d71ccc5aa36cf691616a40bf6fb960fac5620ce53d2f90a95947b90dec509433'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.6.7","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.6.7?os_name=alpine&os_version=3.18"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575a0f523e10e3804eaad37ae18a0a9925ac06fd2c79f918c3037e3ea2fff59d`  
		Last Modified: Sat, 27 Jan 2024 00:53:13 GMT  
		Size: 121.8 MB (121829538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91178239470bfb5a9fb97f8bb8deb2893e907ee6242a1f94621084719e012fba`  
		Last Modified: Sat, 27 Jan 2024 00:53:10 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.6-alpine3.18` - unknown; unknown

```console
$ docker pull julia@sha256:9154f6cc97d896902e2ec19c461a83e85ac0cf77aee5f4c276721011d9b0b383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.5 KB (78523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ebb2b48eccf48a6261fded6da11e6c25f0054ebcf24c7dada94409e881fb175`

```dockerfile
```

-	Layers:
	-	`sha256:aa085a86ddc0ec065af7682e985b28206e9f0735f0aa2eda81ea7f4f5316c8af`  
		Last Modified: Sat, 27 Jan 2024 00:53:10 GMT  
		Size: 65.7 KB (65669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d634cf7f77f7db0f27fa39b6643528578afe78a11454726420f5470de41b887e`  
		Last Modified: Sat, 27 Jan 2024 00:53:10 GMT  
		Size: 12.9 KB (12854 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.6-alpine3.19`

```console
$ docker pull julia@sha256:634e2b295d1a176d57a87bf6ad3916546ad9b36922aed24f39d20ac3df909847
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.6-alpine3.19` - linux; amd64

```console
$ docker pull julia@sha256:e2eab0dc4aed438d27d8e47e2b82c6d73e1a9f9736f59d3a0c051c9de65b32f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125238430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a0efb053006ce1a2c3acfb4e228edffc8c81dae4084f828a702d3ae3ae97e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 09 Dec 2023 15:29:30 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 09 Dec 2023 15:29:30 GMT
CMD ["/bin/sh"]
# Sat, 09 Dec 2023 15:29:30 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 09 Dec 2023 15:29:30 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Dec 2023 15:29:30 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 09 Dec 2023 15:29:30 GMT
ENV JULIA_VERSION=1.6.7
# Sat, 09 Dec 2023 15:29:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.6/julia-1.6.7-musl-x86_64.tar.gz'; 			sha256='d71ccc5aa36cf691616a40bf6fb960fac5620ce53d2f90a95947b90dec509433'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.6.7","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.6.7?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Sat, 09 Dec 2023 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 09 Dec 2023 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 09 Dec 2023 15:29:30 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69e0de20d2a2b103d3b92574c30d8e9edbfd15063f4dc3067ca122c50f83b9e`  
		Last Modified: Sat, 27 Jan 2024 00:53:09 GMT  
		Size: 121.8 MB (121829335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52371be8dc23f0d60deb16f0ec1425dc62e573d5c39394fa1fb31e5e19cc21a0`  
		Last Modified: Sat, 27 Jan 2024 00:53:08 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.6-alpine3.19` - unknown; unknown

```console
$ docker pull julia@sha256:da13ca697ea7277d0b9c37e966074fffb314bc6f390ed83340fb4860b72d9287
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.3 KB (80300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bb702dac0ec1518fe072dec676ce70592eca8bef920b99ee3f79258cd15e20b`

```dockerfile
```

-	Layers:
	-	`sha256:61d23b6ea854fd54b94ca4cfa3c6c7033477f5f84165bb6f79e813b6360b5c16`  
		Last Modified: Sat, 27 Jan 2024 00:53:07 GMT  
		Size: 66.8 KB (66835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79f4dfe8c80354d2b8d2ea8a77d7a83f446322f3be7afe42462a8cbbe70df78e`  
		Last Modified: Sat, 27 Jan 2024 00:53:07 GMT  
		Size: 13.5 KB (13465 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.6-bookworm`

```console
$ docker pull julia@sha256:c676e13c279d07d3d8d155a84ac46efefdc34a488779dfb92370a49c4ada6736
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.6-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:1e9c9aa0fa242fb4b3a7fb6f67d212a104a2b646edc398128371df8cfe271e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.3 MB (157256279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52873e5ddddf1bd9c9acd2701a47c05e87cb3abe5611c66e947122d2cc09b9bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 10 Nov 2023 15:26:46 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["bash"]
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 10 Nov 2023 15:26:46 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_VERSION=1.6.7
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.6.7","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.6.7?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbdf56e13c93bec7604b443c61718b2b2a556d76f9b2b9d51164899250e09069`  
		Last Modified: Tue, 13 Feb 2024 01:53:46 GMT  
		Size: 5.7 MB (5707962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697dbd1cfee9c43d7f4b9763a6c332d5a0505ad0d54e29efd9e62b49b23b9c33`  
		Last Modified: Tue, 13 Feb 2024 01:53:48 GMT  
		Size: 122.4 MB (122423862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c54cf712f8283756f4fa342c9e3577ce4cfcb42f0975fc7b1b9c7e5e7043e6`  
		Last Modified: Tue, 13 Feb 2024 01:53:46 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.6-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:df9cb8c425d0f409537a377661e2d514e16748f8eca85f1c98cfb7b839217d45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2133576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2f0a6c822c077b461b1b0aa885073889a6b7078ca912e3da6faee11e011d40`

```dockerfile
```

-	Layers:
	-	`sha256:14720befa9fad15710243ce7eaf791a52abf6ba5ae772e45b518b78140d4e385`  
		Last Modified: Tue, 13 Feb 2024 01:53:46 GMT  
		Size: 2.1 MB (2115456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89725b6fcddd4182ef8fb630912e0a1c3d5f2992cb869ef2eaf259437c7c75c2`  
		Last Modified: Tue, 13 Feb 2024 01:53:46 GMT  
		Size: 18.1 KB (18120 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.6-bookworm` - linux; arm variant v7

```console
$ docker pull julia@sha256:35e94e8db589a16b8ddfad20270179bf4dec5fba02f6c83c02f3eaa9cf587e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142847407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b0f754906fefef55f2be2902877bac1776e86f927760a9360761a644c8848f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 10 Nov 2023 15:26:46 GMT
ADD file:d6072ced9736ca566086eea2514cf12faccec9859bbd93e83950ad51f6827e8c in / 
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["bash"]
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 10 Nov 2023 15:26:46 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_VERSION=1.6.7
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.6.7","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.6.7?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:404006a0fd99beed6ef1a9502692bd5005ae8c3b9d36a9b48654f7dfaacfb2c5`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 24.7 MB (24741565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c1ff3c5af224419230c243f5e6ed677cbc45ce6989c3d02bb48009914ff039`  
		Last Modified: Sat, 03 Feb 2024 11:33:25 GMT  
		Size: 4.6 MB (4632669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75bee3d1565fcf900a80fcdf2213b4ae67c4d862f29b584b60f80d7d448fb02`  
		Last Modified: Sat, 03 Feb 2024 11:33:28 GMT  
		Size: 113.5 MB (113472799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60106ec0de297b8ce826f05530ce5fbc7eaaa253a1620c3a79403b6e0c9c64ac`  
		Last Modified: Sat, 03 Feb 2024 11:33:24 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.6-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:9de087a177e288c87696be457794ac43b526a03676f70dadf572d901c7924c50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:859525c46727f8495f9e894f5efe5182f220d71ee2dbdb90745e72624f6a8067`

```dockerfile
```

-	Layers:
	-	`sha256:c98f5c67982985c4ff6851cec3dc6551bf3b3e0389d2949a0f20a6038c014989`  
		Last Modified: Sat, 03 Feb 2024 11:33:25 GMT  
		Size: 2.1 MB (2117788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1a3c9f6334d0291d9164ed89ec6e61e2a177792327bbbc99868cac176cbb4d1`  
		Last Modified: Sat, 03 Feb 2024 11:33:24 GMT  
		Size: 18.0 KB (18035 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.6-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:512b438acf54e6bcd1834955126f91210011cabeb171730d33368e7ef49d6a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150901838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aeac16aeed7ef952e0ecd3dc455f2b54fb6cfef91ec778b71e233d4f7ed2321`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 10 Nov 2023 15:26:46 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["bash"]
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 10 Nov 2023 15:26:46 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_VERSION=1.6.7
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.6.7","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.6.7?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b14e605bd6638a1976eeb8d1cde59556a1f77295bac46d1669a9e27e6cd0ad6`  
		Last Modified: Wed, 14 Feb 2024 00:40:29 GMT  
		Size: 5.5 MB (5533149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebde71b115cbf7bafbe0d4417955686065606fe2fa767fc6ed31d12ae4926ba4`  
		Last Modified: Wed, 14 Feb 2024 00:42:29 GMT  
		Size: 116.2 MB (116211958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9451bb0011bcbf1daf2d00410a734f9750c021ad8aebe4d391a64fdb3e1971d1`  
		Last Modified: Wed, 14 Feb 2024 00:42:26 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.6-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:8cc763722290d52ec2b1a7fa18c628d2630411b0bbe1a661cac3fb2ec2bb4151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2133754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77fa3a8b17893a35d1023aa52f8adc2684a373d93191eb7ca6260843a1a6b170`

```dockerfile
```

-	Layers:
	-	`sha256:63a9b0ef4a753f8b9fb3fd2346a01b6aa5480cd222052744cf4b000957a1a1b9`  
		Last Modified: Wed, 14 Feb 2024 00:42:26 GMT  
		Size: 2.1 MB (2115791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6f7b5d56798cccc7af9f29454a32b0ef2b633c7c8e51e585db5877186617942`  
		Last Modified: Wed, 14 Feb 2024 00:42:26 GMT  
		Size: 18.0 KB (17963 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.6-bookworm` - linux; 386

```console
$ docker pull julia@sha256:33f51106daf2cb9f30fe8d9b9062b7b5f81ee6077ce736da915ca0d0310fb9de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156096437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85a982556a5c23ceeb73b8cbf696d3d6a06acc7aa74109a3eae1a627756648e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 10 Nov 2023 15:26:46 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["bash"]
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 10 Nov 2023 15:26:46 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_VERSION=1.6.7
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.6.7","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.6.7?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f077852809d3df0ff0aaa7a7999f678d46ef0610856b3cdfeb43cfa4f5640b9`  
		Last Modified: Tue, 13 Feb 2024 01:53:50 GMT  
		Size: 5.9 MB (5863266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1f1076a2abdc9cee969fb84b5be03f8fa38280081598bd24a7d3571754d0e8`  
		Last Modified: Tue, 13 Feb 2024 01:53:53 GMT  
		Size: 120.1 MB (120090994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8cc012aa6af202e8c794bdeefa180135dd62b2d847c2de62028bb0d8f7d3ec`  
		Last Modified: Tue, 13 Feb 2024 01:53:50 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.6-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:591fbb52b8d270de8a94e59e0b76349486c19676866f93ac08fcbc0723755ff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2130741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9492628cf08b5352cfb403a015a7c43586f5f454e1457e5e00619820fed796b4`

```dockerfile
```

-	Layers:
	-	`sha256:a838468fc0caa024ea0293c369b3c4b3704212fd01d445d6e48389a9fae99d63`  
		Last Modified: Tue, 13 Feb 2024 01:53:50 GMT  
		Size: 2.1 MB (2112654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:195d2faeee1d99524485898b2275f5c342519a2088c7821a5981b3aa95aff7cf`  
		Last Modified: Tue, 13 Feb 2024 01:53:50 GMT  
		Size: 18.1 KB (18087 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.6-bullseye`

```console
$ docker pull julia@sha256:e0fddb0b232aa234ec0cd86aa9bed756249f86b3cedf5dabd543b213ccaa399d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.6-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:ae93e84f40b527b886c50aa4e778d752a93f67c8eeb5ccc47fbbde8a4b3ad751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.3 MB (156273540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e9a8aa572dcbf8bcbcabc32a448cc737b3fad7cacba953b096e7160f6f57b3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 10 Nov 2023 15:26:46 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["bash"]
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 10 Nov 2023 15:26:46 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_VERSION=1.6.7
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.6.7","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.6.7?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44055ebbad9a840edd272723b88393e077281ccca3a1b698a3d44b26563cae8e`  
		Last Modified: Tue, 13 Feb 2024 01:53:46 GMT  
		Size: 2.4 MB (2426505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f6e5deb2eac362f8750eddaad28bf4f5d4e151edd12382369644f9e8d53834`  
		Last Modified: Tue, 13 Feb 2024 01:53:48 GMT  
		Size: 122.4 MB (122424246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e96350ebccfd7a4233369bfd04632aa48f1b42fe8bc74332302521f0c557d78`  
		Last Modified: Tue, 13 Feb 2024 01:53:46 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.6-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:82db38e2c28e78689c893ea49525d25ce922b8cb7a3e4e9e0965c7446d032baa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2354084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c1d7019ada9a32c38a25e9a25c469bb25e8e1aef8f4124b4aec63aea1063660`

```dockerfile
```

-	Layers:
	-	`sha256:9b4bde1258c12fc31e0a0e43a465f3387b238b5ec05a2c1b6736190460b9a5aa`  
		Last Modified: Tue, 13 Feb 2024 01:53:46 GMT  
		Size: 2.3 MB (2336548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:faeb5bdda1ddfe200c6a09badaac3b6663d765788475daa796bea35d8f2cdb62`  
		Last Modified: Tue, 13 Feb 2024 01:53:46 GMT  
		Size: 17.5 KB (17536 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.6-bullseye` - linux; arm variant v7

```console
$ docker pull julia@sha256:166a3c80fe18f6af1fb4ee062820e8cc3d13bdfb796bf6a440bd0f74860626ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142077562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3194d7833dbcaa7dce91eda133eb75e4a0e1e9b1f7ce9000e8a51291c7df7044`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 10 Nov 2023 15:26:46 GMT
ADD file:65b9e2efdf2b09faf0d5ea0e2e00984ff3c8cf89b7959287bc6ca54c7772801d in / 
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["bash"]
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 10 Nov 2023 15:26:46 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_VERSION=1.6.7
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.6.7","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.6.7?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4de6a546d77461a35cb9514c6432142adfb72460cf04bac21bd261d66c288476`  
		Last Modified: Wed, 31 Jan 2024 22:49:36 GMT  
		Size: 26.6 MB (26579212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5231778797bc56a4a08ab1f98a7404c0ce93eba8510a46cb8cfa5cc105b33787`  
		Last Modified: Sat, 03 Feb 2024 11:35:00 GMT  
		Size: 2.0 MB (2025850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca298d55f5af2ac1229b547303326aaa61682035cefda0e23a8663fbf4da4a8`  
		Last Modified: Sat, 03 Feb 2024 11:35:03 GMT  
		Size: 113.5 MB (113472127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f863e5ff6e69d1c00d6dd2e5d868f67670607ebe5adf245b4b3a146b4366d209`  
		Last Modified: Sat, 03 Feb 2024 11:35:00 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.6-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:e3855ff86bd536f471d2e159ee3d2f9e91aae035551272b3aec98139458885db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2264566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8e365ee64c374ebdbac5392b32bbe79ea9fdc93134ece6269ad3f7837a3e5e5`

```dockerfile
```

-	Layers:
	-	`sha256:383e5a8123f306e0d60e7c11d64b25f830595aa16c73879f60c21a87981b37f3`  
		Last Modified: Sat, 03 Feb 2024 11:35:00 GMT  
		Size: 2.2 MB (2247130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c1413c4451427a6e8345c839f48a9fb1501e8cececcad57338c87c5a0871a0e`  
		Last Modified: Sat, 03 Feb 2024 11:35:00 GMT  
		Size: 17.4 KB (17436 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.6-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:f547698892cdc1d19af623341188826eb0edc5b15e132f5f5027e48ab9b14e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148698555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9afba32909e96b304eddd83ab804f6487753adfc8add922f36413c95ec4f46d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 10 Nov 2023 15:26:46 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["bash"]
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 10 Nov 2023 15:26:46 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_VERSION=1.6.7
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.6.7","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.6.7?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1acd381bc5ce074386a44640a70f3d2d53921e7cda7c6386a20616c9fab4cee5`  
		Last Modified: Wed, 14 Feb 2024 00:41:34 GMT  
		Size: 2.4 MB (2415040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c90b692c61af45526b067b1bf1b2ceb13322db12eee47fbe8f1cc1a96d89609`  
		Last Modified: Wed, 14 Feb 2024 00:43:16 GMT  
		Size: 116.2 MB (116212069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1eb6a1cae9a6a5309398434109d4a94bbd1ec71ef01f09ab8a64a211a5b14b`  
		Last Modified: Wed, 14 Feb 2024 00:43:12 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.6-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:59551459df38eaacc35fdc3b8cea8f9e26214868c9943218cb196d38b559d13d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2354244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f30befc2b480479913e1a574a4d602ae24fc0d0f1761b1c8212036a7e8a9da3`

```dockerfile
```

-	Layers:
	-	`sha256:578a1641140e2764a9b5b86a0b77b591b42e0ec193255acd1b6cbb1eaad391c1`  
		Last Modified: Wed, 14 Feb 2024 00:43:13 GMT  
		Size: 2.3 MB (2336869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60187de5d671b93e104cc6ce28301c7f9a269b4c44df1f2c1b6adeca6db6e9a8`  
		Last Modified: Wed, 14 Feb 2024 00:43:12 GMT  
		Size: 17.4 KB (17375 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.6-bullseye` - linux; 386

```console
$ docker pull julia@sha256:519503c3933ece0eea52e55edfae5f9544474a717d1b9b24f3fde56b8f7c45f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.0 MB (155031210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:146d6c24a377c4bce3621687747a06a0a575aab993166f04da5dbd93236a46cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 10 Nov 2023 15:26:46 GMT
ADD file:9eaee5af136d095dc1dac0ffce0fde09d8f1bd02ff7cb65ee67e00b2a66f34f7 in / 
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["bash"]
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 10 Nov 2023 15:26:46 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_VERSION=1.6.7
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.6.7","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.6.7?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1ac8173b08d16f9f136fb0e3ee39999cef7495f924ecb43f3ca4a4eea267cc88`  
		Last Modified: Tue, 13 Feb 2024 00:44:36 GMT  
		Size: 32.4 MB (32407443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88194674edbd99cb92bce2bf868fbcbfa1f9e3705fd917a20de4f7c9348380f8`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 2.5 MB (2533059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3772b84a9011053ab51ee0620e3020ffac7503a8d7ec421bd5993500ed179d`  
		Last Modified: Tue, 13 Feb 2024 01:53:58 GMT  
		Size: 120.1 MB (120090340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7caf8fda699f4879be705ad5ba0cc80939ac60a77f94801a05d3adc6710e1b`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.6-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:b1997b9cb6650ef1915f3585b569cf8f35f99859600a6f78e7f279bff3869a6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2351279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecccd630382a36d25e217634cff89737577676dc09de2fb845d9b9d28b1a8e3c`

```dockerfile
```

-	Layers:
	-	`sha256:5ec454dc25b4c298a3a1cf315339c2bf11d6b455a694e218fb8b26782e967393`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 2.3 MB (2333764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec66f549b1093d1f19ee98fb6f4a133764488bec8ef952548f7b315aac4b4633`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 17.5 KB (17515 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.6-windowsservercore`

```console
$ docker pull julia@sha256:c2f87c3d76e487009bdca4540789a155dbb7b336389b817e215cc3c02f20e999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `julia:1.6-windowsservercore` - windows version 10.0.20348.2227; amd64

```console
$ docker pull julia@sha256:aacbbc8940601c0e5596931fa9d41cce28ab1fa2c31c78c1d116e219483534c7
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2034764054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:543f707ae687e7e690271d7fe6f8b11b7c62dc6f786e23fee7dadc2b52c6351e`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Thu, 11 Jan 2024 00:08:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:08:01 GMT
ENV JULIA_VERSION=1.6.7
# Thu, 11 Jan 2024 00:08:02 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Thu, 11 Jan 2024 00:08:02 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Thu, 11 Jan 2024 00:08:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:08:50 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ec27c9842b8e899a5278c55aa21d2cf14e62ae5b8dbc8ef21ffe38683f694d`  
		Last Modified: Thu, 11 Jan 2024 00:08:56 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12f858d296dd90c13c42516bcc60fae65f52207d2846a54ad3e3c059b87bf85`  
		Last Modified: Thu, 11 Jan 2024 00:08:54 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37065f76f4d697c310167b0cf169601492542ffeb7174129d6077ec8af74ff49`  
		Last Modified: Thu, 11 Jan 2024 00:08:54 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b334853e6c04835809903c081d10c7faa8ee0d9d6d3684d89e8d6954e2725c5`  
		Last Modified: Thu, 11 Jan 2024 00:08:54 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109a7946e539e9a6238d5492f541cd7ce6b55b428fdf1d34f9ead65ac74bb682`  
		Last Modified: Thu, 11 Jan 2024 00:09:12 GMT  
		Size: 134.5 MB (134544929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35917c15fff017c85a175e4c462c3fc80c624510736cf63a746358851e462b7f`  
		Last Modified: Thu, 11 Jan 2024 00:08:54 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6-windowsservercore` - windows version 10.0.17763.5329; amd64

```console
$ docker pull julia@sha256:09f0a64aa6af42e12b9c0667122016bbda84151ebbc217b59fc24aa875e3e953
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2204271920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2770e04b2d617a0710f509eaa78ee9e3db8e0c4742f63c90e174a5277fb3889`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:04:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:04:59 GMT
ENV JULIA_VERSION=1.6.7
# Thu, 11 Jan 2024 00:05:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Thu, 11 Jan 2024 00:05:01 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Thu, 11 Jan 2024 00:06:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:06:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018567616bba50c617270b645f6f9f5eeffc82add802ee321a43b1cbcabf047d`  
		Last Modified: Thu, 11 Jan 2024 00:06:29 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f16287f2b89a420c3c6ff9e6b119a9bac0bca4711c2c38160c6725a076af14a`  
		Last Modified: Thu, 11 Jan 2024 00:06:27 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b9460df90a5ea657a924cb2e8e06f9d231da0255adfe2727c85142c3b9acbff`  
		Last Modified: Thu, 11 Jan 2024 00:06:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2307766466bf7a0f3659aed4269cb3895dde01f7f7d2eb6bf4a40a5893ac05b`  
		Last Modified: Thu, 11 Jan 2024 00:06:27 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaceb21bd3ac6440c397b6e7b9de7788c1019a0f1ed396375f20819fb2e82d1`  
		Last Modified: Thu, 11 Jan 2024 00:06:45 GMT  
		Size: 134.5 MB (134542902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4ebe971903a073c38f33636a0c5c3435c9abef3f9e10437c9b35e51c33e674`  
		Last Modified: Thu, 11 Jan 2024 00:06:27 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6-windowsservercore-1809`

```console
$ docker pull julia@sha256:e6acba1d8d740dd47c572f3fe4637b29247fe6a6924c7ea2d050f09f4747a2e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `julia:1.6-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull julia@sha256:09f0a64aa6af42e12b9c0667122016bbda84151ebbc217b59fc24aa875e3e953
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2204271920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2770e04b2d617a0710f509eaa78ee9e3db8e0c4742f63c90e174a5277fb3889`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:04:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:04:59 GMT
ENV JULIA_VERSION=1.6.7
# Thu, 11 Jan 2024 00:05:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Thu, 11 Jan 2024 00:05:01 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Thu, 11 Jan 2024 00:06:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:06:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018567616bba50c617270b645f6f9f5eeffc82add802ee321a43b1cbcabf047d`  
		Last Modified: Thu, 11 Jan 2024 00:06:29 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f16287f2b89a420c3c6ff9e6b119a9bac0bca4711c2c38160c6725a076af14a`  
		Last Modified: Thu, 11 Jan 2024 00:06:27 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b9460df90a5ea657a924cb2e8e06f9d231da0255adfe2727c85142c3b9acbff`  
		Last Modified: Thu, 11 Jan 2024 00:06:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2307766466bf7a0f3659aed4269cb3895dde01f7f7d2eb6bf4a40a5893ac05b`  
		Last Modified: Thu, 11 Jan 2024 00:06:27 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaceb21bd3ac6440c397b6e7b9de7788c1019a0f1ed396375f20819fb2e82d1`  
		Last Modified: Thu, 11 Jan 2024 00:06:45 GMT  
		Size: 134.5 MB (134542902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4ebe971903a073c38f33636a0c5c3435c9abef3f9e10437c9b35e51c33e674`  
		Last Modified: Thu, 11 Jan 2024 00:06:27 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:afbab72fbecd773fc4aba01df3cf9a781228c934da8685c8a59704922a00edb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `julia:1.6-windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull julia@sha256:aacbbc8940601c0e5596931fa9d41cce28ab1fa2c31c78c1d116e219483534c7
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2034764054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:543f707ae687e7e690271d7fe6f8b11b7c62dc6f786e23fee7dadc2b52c6351e`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Thu, 11 Jan 2024 00:08:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:08:01 GMT
ENV JULIA_VERSION=1.6.7
# Thu, 11 Jan 2024 00:08:02 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Thu, 11 Jan 2024 00:08:02 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Thu, 11 Jan 2024 00:08:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:08:50 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ec27c9842b8e899a5278c55aa21d2cf14e62ae5b8dbc8ef21ffe38683f694d`  
		Last Modified: Thu, 11 Jan 2024 00:08:56 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12f858d296dd90c13c42516bcc60fae65f52207d2846a54ad3e3c059b87bf85`  
		Last Modified: Thu, 11 Jan 2024 00:08:54 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37065f76f4d697c310167b0cf169601492542ffeb7174129d6077ec8af74ff49`  
		Last Modified: Thu, 11 Jan 2024 00:08:54 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b334853e6c04835809903c081d10c7faa8ee0d9d6d3684d89e8d6954e2725c5`  
		Last Modified: Thu, 11 Jan 2024 00:08:54 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109a7946e539e9a6238d5492f541cd7ce6b55b428fdf1d34f9ead65ac74bb682`  
		Last Modified: Thu, 11 Jan 2024 00:09:12 GMT  
		Size: 134.5 MB (134544929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35917c15fff017c85a175e4c462c3fc80c624510736cf63a746358851e462b7f`  
		Last Modified: Thu, 11 Jan 2024 00:08:54 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6.7`

```console
$ docker pull julia@sha256:d68eedb4de05d8840076683de1e4abe751a4b4d0c67c02c0127f99605a937a41
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `julia:1.6.7` - linux; amd64

```console
$ docker pull julia@sha256:1e9c9aa0fa242fb4b3a7fb6f67d212a104a2b646edc398128371df8cfe271e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.3 MB (157256279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52873e5ddddf1bd9c9acd2701a47c05e87cb3abe5611c66e947122d2cc09b9bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 10 Nov 2023 15:26:46 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["bash"]
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 10 Nov 2023 15:26:46 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_VERSION=1.6.7
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.6.7","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.6.7?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbdf56e13c93bec7604b443c61718b2b2a556d76f9b2b9d51164899250e09069`  
		Last Modified: Tue, 13 Feb 2024 01:53:46 GMT  
		Size: 5.7 MB (5707962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697dbd1cfee9c43d7f4b9763a6c332d5a0505ad0d54e29efd9e62b49b23b9c33`  
		Last Modified: Tue, 13 Feb 2024 01:53:48 GMT  
		Size: 122.4 MB (122423862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c54cf712f8283756f4fa342c9e3577ce4cfcb42f0975fc7b1b9c7e5e7043e6`  
		Last Modified: Tue, 13 Feb 2024 01:53:46 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.6.7` - unknown; unknown

```console
$ docker pull julia@sha256:df9cb8c425d0f409537a377661e2d514e16748f8eca85f1c98cfb7b839217d45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2133576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2f0a6c822c077b461b1b0aa885073889a6b7078ca912e3da6faee11e011d40`

```dockerfile
```

-	Layers:
	-	`sha256:14720befa9fad15710243ce7eaf791a52abf6ba5ae772e45b518b78140d4e385`  
		Last Modified: Tue, 13 Feb 2024 01:53:46 GMT  
		Size: 2.1 MB (2115456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89725b6fcddd4182ef8fb630912e0a1c3d5f2992cb869ef2eaf259437c7c75c2`  
		Last Modified: Tue, 13 Feb 2024 01:53:46 GMT  
		Size: 18.1 KB (18120 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.6.7` - linux; arm variant v7

```console
$ docker pull julia@sha256:35e94e8db589a16b8ddfad20270179bf4dec5fba02f6c83c02f3eaa9cf587e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142847407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b0f754906fefef55f2be2902877bac1776e86f927760a9360761a644c8848f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 10 Nov 2023 15:26:46 GMT
ADD file:d6072ced9736ca566086eea2514cf12faccec9859bbd93e83950ad51f6827e8c in / 
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["bash"]
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 10 Nov 2023 15:26:46 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_VERSION=1.6.7
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.6.7","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.6.7?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:404006a0fd99beed6ef1a9502692bd5005ae8c3b9d36a9b48654f7dfaacfb2c5`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 24.7 MB (24741565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c1ff3c5af224419230c243f5e6ed677cbc45ce6989c3d02bb48009914ff039`  
		Last Modified: Sat, 03 Feb 2024 11:33:25 GMT  
		Size: 4.6 MB (4632669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75bee3d1565fcf900a80fcdf2213b4ae67c4d862f29b584b60f80d7d448fb02`  
		Last Modified: Sat, 03 Feb 2024 11:33:28 GMT  
		Size: 113.5 MB (113472799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60106ec0de297b8ce826f05530ce5fbc7eaaa253a1620c3a79403b6e0c9c64ac`  
		Last Modified: Sat, 03 Feb 2024 11:33:24 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.6.7` - unknown; unknown

```console
$ docker pull julia@sha256:9de087a177e288c87696be457794ac43b526a03676f70dadf572d901c7924c50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:859525c46727f8495f9e894f5efe5182f220d71ee2dbdb90745e72624f6a8067`

```dockerfile
```

-	Layers:
	-	`sha256:c98f5c67982985c4ff6851cec3dc6551bf3b3e0389d2949a0f20a6038c014989`  
		Last Modified: Sat, 03 Feb 2024 11:33:25 GMT  
		Size: 2.1 MB (2117788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1a3c9f6334d0291d9164ed89ec6e61e2a177792327bbbc99868cac176cbb4d1`  
		Last Modified: Sat, 03 Feb 2024 11:33:24 GMT  
		Size: 18.0 KB (18035 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.6.7` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:512b438acf54e6bcd1834955126f91210011cabeb171730d33368e7ef49d6a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150901838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aeac16aeed7ef952e0ecd3dc455f2b54fb6cfef91ec778b71e233d4f7ed2321`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 10 Nov 2023 15:26:46 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["bash"]
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 10 Nov 2023 15:26:46 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_VERSION=1.6.7
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.6.7","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.6.7?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b14e605bd6638a1976eeb8d1cde59556a1f77295bac46d1669a9e27e6cd0ad6`  
		Last Modified: Wed, 14 Feb 2024 00:40:29 GMT  
		Size: 5.5 MB (5533149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebde71b115cbf7bafbe0d4417955686065606fe2fa767fc6ed31d12ae4926ba4`  
		Last Modified: Wed, 14 Feb 2024 00:42:29 GMT  
		Size: 116.2 MB (116211958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9451bb0011bcbf1daf2d00410a734f9750c021ad8aebe4d391a64fdb3e1971d1`  
		Last Modified: Wed, 14 Feb 2024 00:42:26 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.6.7` - unknown; unknown

```console
$ docker pull julia@sha256:8cc763722290d52ec2b1a7fa18c628d2630411b0bbe1a661cac3fb2ec2bb4151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2133754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77fa3a8b17893a35d1023aa52f8adc2684a373d93191eb7ca6260843a1a6b170`

```dockerfile
```

-	Layers:
	-	`sha256:63a9b0ef4a753f8b9fb3fd2346a01b6aa5480cd222052744cf4b000957a1a1b9`  
		Last Modified: Wed, 14 Feb 2024 00:42:26 GMT  
		Size: 2.1 MB (2115791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6f7b5d56798cccc7af9f29454a32b0ef2b633c7c8e51e585db5877186617942`  
		Last Modified: Wed, 14 Feb 2024 00:42:26 GMT  
		Size: 18.0 KB (17963 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.6.7` - linux; 386

```console
$ docker pull julia@sha256:33f51106daf2cb9f30fe8d9b9062b7b5f81ee6077ce736da915ca0d0310fb9de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156096437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85a982556a5c23ceeb73b8cbf696d3d6a06acc7aa74109a3eae1a627756648e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 10 Nov 2023 15:26:46 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["bash"]
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 10 Nov 2023 15:26:46 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_VERSION=1.6.7
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.6.7","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.6.7?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f077852809d3df0ff0aaa7a7999f678d46ef0610856b3cdfeb43cfa4f5640b9`  
		Last Modified: Tue, 13 Feb 2024 01:53:50 GMT  
		Size: 5.9 MB (5863266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1f1076a2abdc9cee969fb84b5be03f8fa38280081598bd24a7d3571754d0e8`  
		Last Modified: Tue, 13 Feb 2024 01:53:53 GMT  
		Size: 120.1 MB (120090994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8cc012aa6af202e8c794bdeefa180135dd62b2d847c2de62028bb0d8f7d3ec`  
		Last Modified: Tue, 13 Feb 2024 01:53:50 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.6.7` - unknown; unknown

```console
$ docker pull julia@sha256:591fbb52b8d270de8a94e59e0b76349486c19676866f93ac08fcbc0723755ff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2130741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9492628cf08b5352cfb403a015a7c43586f5f454e1457e5e00619820fed796b4`

```dockerfile
```

-	Layers:
	-	`sha256:a838468fc0caa024ea0293c369b3c4b3704212fd01d445d6e48389a9fae99d63`  
		Last Modified: Tue, 13 Feb 2024 01:53:50 GMT  
		Size: 2.1 MB (2112654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:195d2faeee1d99524485898b2275f5c342519a2088c7821a5981b3aa95aff7cf`  
		Last Modified: Tue, 13 Feb 2024 01:53:50 GMT  
		Size: 18.1 KB (18087 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.6.7` - windows version 10.0.20348.2227; amd64

```console
$ docker pull julia@sha256:aacbbc8940601c0e5596931fa9d41cce28ab1fa2c31c78c1d116e219483534c7
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2034764054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:543f707ae687e7e690271d7fe6f8b11b7c62dc6f786e23fee7dadc2b52c6351e`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Thu, 11 Jan 2024 00:08:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:08:01 GMT
ENV JULIA_VERSION=1.6.7
# Thu, 11 Jan 2024 00:08:02 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Thu, 11 Jan 2024 00:08:02 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Thu, 11 Jan 2024 00:08:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:08:50 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ec27c9842b8e899a5278c55aa21d2cf14e62ae5b8dbc8ef21ffe38683f694d`  
		Last Modified: Thu, 11 Jan 2024 00:08:56 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12f858d296dd90c13c42516bcc60fae65f52207d2846a54ad3e3c059b87bf85`  
		Last Modified: Thu, 11 Jan 2024 00:08:54 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37065f76f4d697c310167b0cf169601492542ffeb7174129d6077ec8af74ff49`  
		Last Modified: Thu, 11 Jan 2024 00:08:54 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b334853e6c04835809903c081d10c7faa8ee0d9d6d3684d89e8d6954e2725c5`  
		Last Modified: Thu, 11 Jan 2024 00:08:54 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109a7946e539e9a6238d5492f541cd7ce6b55b428fdf1d34f9ead65ac74bb682`  
		Last Modified: Thu, 11 Jan 2024 00:09:12 GMT  
		Size: 134.5 MB (134544929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35917c15fff017c85a175e4c462c3fc80c624510736cf63a746358851e462b7f`  
		Last Modified: Thu, 11 Jan 2024 00:08:54 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6.7` - windows version 10.0.17763.5329; amd64

```console
$ docker pull julia@sha256:09f0a64aa6af42e12b9c0667122016bbda84151ebbc217b59fc24aa875e3e953
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2204271920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2770e04b2d617a0710f509eaa78ee9e3db8e0c4742f63c90e174a5277fb3889`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:04:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:04:59 GMT
ENV JULIA_VERSION=1.6.7
# Thu, 11 Jan 2024 00:05:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Thu, 11 Jan 2024 00:05:01 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Thu, 11 Jan 2024 00:06:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:06:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018567616bba50c617270b645f6f9f5eeffc82add802ee321a43b1cbcabf047d`  
		Last Modified: Thu, 11 Jan 2024 00:06:29 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f16287f2b89a420c3c6ff9e6b119a9bac0bca4711c2c38160c6725a076af14a`  
		Last Modified: Thu, 11 Jan 2024 00:06:27 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b9460df90a5ea657a924cb2e8e06f9d231da0255adfe2727c85142c3b9acbff`  
		Last Modified: Thu, 11 Jan 2024 00:06:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2307766466bf7a0f3659aed4269cb3895dde01f7f7d2eb6bf4a40a5893ac05b`  
		Last Modified: Thu, 11 Jan 2024 00:06:27 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaceb21bd3ac6440c397b6e7b9de7788c1019a0f1ed396375f20819fb2e82d1`  
		Last Modified: Thu, 11 Jan 2024 00:06:45 GMT  
		Size: 134.5 MB (134542902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4ebe971903a073c38f33636a0c5c3435c9abef3f9e10437c9b35e51c33e674`  
		Last Modified: Thu, 11 Jan 2024 00:06:27 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6.7-alpine`

```console
$ docker pull julia@sha256:634e2b295d1a176d57a87bf6ad3916546ad9b36922aed24f39d20ac3df909847
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.6.7-alpine` - linux; amd64

```console
$ docker pull julia@sha256:e2eab0dc4aed438d27d8e47e2b82c6d73e1a9f9736f59d3a0c051c9de65b32f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125238430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a0efb053006ce1a2c3acfb4e228edffc8c81dae4084f828a702d3ae3ae97e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 09 Dec 2023 15:29:30 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 09 Dec 2023 15:29:30 GMT
CMD ["/bin/sh"]
# Sat, 09 Dec 2023 15:29:30 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 09 Dec 2023 15:29:30 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Dec 2023 15:29:30 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 09 Dec 2023 15:29:30 GMT
ENV JULIA_VERSION=1.6.7
# Sat, 09 Dec 2023 15:29:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.6/julia-1.6.7-musl-x86_64.tar.gz'; 			sha256='d71ccc5aa36cf691616a40bf6fb960fac5620ce53d2f90a95947b90dec509433'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.6.7","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.6.7?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Sat, 09 Dec 2023 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 09 Dec 2023 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 09 Dec 2023 15:29:30 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69e0de20d2a2b103d3b92574c30d8e9edbfd15063f4dc3067ca122c50f83b9e`  
		Last Modified: Sat, 27 Jan 2024 00:53:09 GMT  
		Size: 121.8 MB (121829335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52371be8dc23f0d60deb16f0ec1425dc62e573d5c39394fa1fb31e5e19cc21a0`  
		Last Modified: Sat, 27 Jan 2024 00:53:08 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.6.7-alpine` - unknown; unknown

```console
$ docker pull julia@sha256:da13ca697ea7277d0b9c37e966074fffb314bc6f390ed83340fb4860b72d9287
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.3 KB (80300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bb702dac0ec1518fe072dec676ce70592eca8bef920b99ee3f79258cd15e20b`

```dockerfile
```

-	Layers:
	-	`sha256:61d23b6ea854fd54b94ca4cfa3c6c7033477f5f84165bb6f79e813b6360b5c16`  
		Last Modified: Sat, 27 Jan 2024 00:53:07 GMT  
		Size: 66.8 KB (66835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79f4dfe8c80354d2b8d2ea8a77d7a83f446322f3be7afe42462a8cbbe70df78e`  
		Last Modified: Sat, 27 Jan 2024 00:53:07 GMT  
		Size: 13.5 KB (13465 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.6.7-alpine3.18`

```console
$ docker pull julia@sha256:9d3f8d87a4169fd0f722e0f6799c5c774430afd56bb76effc51caa08077dba7a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.6.7-alpine3.18` - linux; amd64

```console
$ docker pull julia@sha256:1db84d51d1be7d36c0e54a8d4ef980f1ad0a5085ce909cf9a3e81fe82db5e4ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125232446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:614e6c7c70e8ac5b7e4711d99c6555a9af8e9b80d5dfc7a27472b7a471b14f7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 10 Nov 2023 15:26:46 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["/bin/sh"]
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 10 Nov 2023 15:26:46 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_VERSION=1.6.7
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.6/julia-1.6.7-musl-x86_64.tar.gz'; 			sha256='d71ccc5aa36cf691616a40bf6fb960fac5620ce53d2f90a95947b90dec509433'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.6.7","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.6.7?os_name=alpine&os_version=3.18"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575a0f523e10e3804eaad37ae18a0a9925ac06fd2c79f918c3037e3ea2fff59d`  
		Last Modified: Sat, 27 Jan 2024 00:53:13 GMT  
		Size: 121.8 MB (121829538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91178239470bfb5a9fb97f8bb8deb2893e907ee6242a1f94621084719e012fba`  
		Last Modified: Sat, 27 Jan 2024 00:53:10 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.6.7-alpine3.18` - unknown; unknown

```console
$ docker pull julia@sha256:9154f6cc97d896902e2ec19c461a83e85ac0cf77aee5f4c276721011d9b0b383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.5 KB (78523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ebb2b48eccf48a6261fded6da11e6c25f0054ebcf24c7dada94409e881fb175`

```dockerfile
```

-	Layers:
	-	`sha256:aa085a86ddc0ec065af7682e985b28206e9f0735f0aa2eda81ea7f4f5316c8af`  
		Last Modified: Sat, 27 Jan 2024 00:53:10 GMT  
		Size: 65.7 KB (65669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d634cf7f77f7db0f27fa39b6643528578afe78a11454726420f5470de41b887e`  
		Last Modified: Sat, 27 Jan 2024 00:53:10 GMT  
		Size: 12.9 KB (12854 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.6.7-alpine3.19`

```console
$ docker pull julia@sha256:634e2b295d1a176d57a87bf6ad3916546ad9b36922aed24f39d20ac3df909847
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.6.7-alpine3.19` - linux; amd64

```console
$ docker pull julia@sha256:e2eab0dc4aed438d27d8e47e2b82c6d73e1a9f9736f59d3a0c051c9de65b32f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125238430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a0efb053006ce1a2c3acfb4e228edffc8c81dae4084f828a702d3ae3ae97e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 09 Dec 2023 15:29:30 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 09 Dec 2023 15:29:30 GMT
CMD ["/bin/sh"]
# Sat, 09 Dec 2023 15:29:30 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 09 Dec 2023 15:29:30 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Dec 2023 15:29:30 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 09 Dec 2023 15:29:30 GMT
ENV JULIA_VERSION=1.6.7
# Sat, 09 Dec 2023 15:29:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.6/julia-1.6.7-musl-x86_64.tar.gz'; 			sha256='d71ccc5aa36cf691616a40bf6fb960fac5620ce53d2f90a95947b90dec509433'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.6.7","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.6.7?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Sat, 09 Dec 2023 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 09 Dec 2023 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 09 Dec 2023 15:29:30 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69e0de20d2a2b103d3b92574c30d8e9edbfd15063f4dc3067ca122c50f83b9e`  
		Last Modified: Sat, 27 Jan 2024 00:53:09 GMT  
		Size: 121.8 MB (121829335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52371be8dc23f0d60deb16f0ec1425dc62e573d5c39394fa1fb31e5e19cc21a0`  
		Last Modified: Sat, 27 Jan 2024 00:53:08 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.6.7-alpine3.19` - unknown; unknown

```console
$ docker pull julia@sha256:da13ca697ea7277d0b9c37e966074fffb314bc6f390ed83340fb4860b72d9287
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.3 KB (80300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bb702dac0ec1518fe072dec676ce70592eca8bef920b99ee3f79258cd15e20b`

```dockerfile
```

-	Layers:
	-	`sha256:61d23b6ea854fd54b94ca4cfa3c6c7033477f5f84165bb6f79e813b6360b5c16`  
		Last Modified: Sat, 27 Jan 2024 00:53:07 GMT  
		Size: 66.8 KB (66835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79f4dfe8c80354d2b8d2ea8a77d7a83f446322f3be7afe42462a8cbbe70df78e`  
		Last Modified: Sat, 27 Jan 2024 00:53:07 GMT  
		Size: 13.5 KB (13465 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.6.7-bookworm`

```console
$ docker pull julia@sha256:c676e13c279d07d3d8d155a84ac46efefdc34a488779dfb92370a49c4ada6736
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.6.7-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:1e9c9aa0fa242fb4b3a7fb6f67d212a104a2b646edc398128371df8cfe271e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.3 MB (157256279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52873e5ddddf1bd9c9acd2701a47c05e87cb3abe5611c66e947122d2cc09b9bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 10 Nov 2023 15:26:46 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["bash"]
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 10 Nov 2023 15:26:46 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_VERSION=1.6.7
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.6.7","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.6.7?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbdf56e13c93bec7604b443c61718b2b2a556d76f9b2b9d51164899250e09069`  
		Last Modified: Tue, 13 Feb 2024 01:53:46 GMT  
		Size: 5.7 MB (5707962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697dbd1cfee9c43d7f4b9763a6c332d5a0505ad0d54e29efd9e62b49b23b9c33`  
		Last Modified: Tue, 13 Feb 2024 01:53:48 GMT  
		Size: 122.4 MB (122423862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c54cf712f8283756f4fa342c9e3577ce4cfcb42f0975fc7b1b9c7e5e7043e6`  
		Last Modified: Tue, 13 Feb 2024 01:53:46 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.6.7-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:df9cb8c425d0f409537a377661e2d514e16748f8eca85f1c98cfb7b839217d45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2133576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2f0a6c822c077b461b1b0aa885073889a6b7078ca912e3da6faee11e011d40`

```dockerfile
```

-	Layers:
	-	`sha256:14720befa9fad15710243ce7eaf791a52abf6ba5ae772e45b518b78140d4e385`  
		Last Modified: Tue, 13 Feb 2024 01:53:46 GMT  
		Size: 2.1 MB (2115456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89725b6fcddd4182ef8fb630912e0a1c3d5f2992cb869ef2eaf259437c7c75c2`  
		Last Modified: Tue, 13 Feb 2024 01:53:46 GMT  
		Size: 18.1 KB (18120 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.6.7-bookworm` - linux; arm variant v7

```console
$ docker pull julia@sha256:35e94e8db589a16b8ddfad20270179bf4dec5fba02f6c83c02f3eaa9cf587e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142847407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b0f754906fefef55f2be2902877bac1776e86f927760a9360761a644c8848f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 10 Nov 2023 15:26:46 GMT
ADD file:d6072ced9736ca566086eea2514cf12faccec9859bbd93e83950ad51f6827e8c in / 
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["bash"]
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 10 Nov 2023 15:26:46 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_VERSION=1.6.7
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.6.7","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.6.7?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:404006a0fd99beed6ef1a9502692bd5005ae8c3b9d36a9b48654f7dfaacfb2c5`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 24.7 MB (24741565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c1ff3c5af224419230c243f5e6ed677cbc45ce6989c3d02bb48009914ff039`  
		Last Modified: Sat, 03 Feb 2024 11:33:25 GMT  
		Size: 4.6 MB (4632669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75bee3d1565fcf900a80fcdf2213b4ae67c4d862f29b584b60f80d7d448fb02`  
		Last Modified: Sat, 03 Feb 2024 11:33:28 GMT  
		Size: 113.5 MB (113472799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60106ec0de297b8ce826f05530ce5fbc7eaaa253a1620c3a79403b6e0c9c64ac`  
		Last Modified: Sat, 03 Feb 2024 11:33:24 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.6.7-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:9de087a177e288c87696be457794ac43b526a03676f70dadf572d901c7924c50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:859525c46727f8495f9e894f5efe5182f220d71ee2dbdb90745e72624f6a8067`

```dockerfile
```

-	Layers:
	-	`sha256:c98f5c67982985c4ff6851cec3dc6551bf3b3e0389d2949a0f20a6038c014989`  
		Last Modified: Sat, 03 Feb 2024 11:33:25 GMT  
		Size: 2.1 MB (2117788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1a3c9f6334d0291d9164ed89ec6e61e2a177792327bbbc99868cac176cbb4d1`  
		Last Modified: Sat, 03 Feb 2024 11:33:24 GMT  
		Size: 18.0 KB (18035 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.6.7-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:512b438acf54e6bcd1834955126f91210011cabeb171730d33368e7ef49d6a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150901838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aeac16aeed7ef952e0ecd3dc455f2b54fb6cfef91ec778b71e233d4f7ed2321`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 10 Nov 2023 15:26:46 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["bash"]
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 10 Nov 2023 15:26:46 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_VERSION=1.6.7
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.6.7","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.6.7?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b14e605bd6638a1976eeb8d1cde59556a1f77295bac46d1669a9e27e6cd0ad6`  
		Last Modified: Wed, 14 Feb 2024 00:40:29 GMT  
		Size: 5.5 MB (5533149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebde71b115cbf7bafbe0d4417955686065606fe2fa767fc6ed31d12ae4926ba4`  
		Last Modified: Wed, 14 Feb 2024 00:42:29 GMT  
		Size: 116.2 MB (116211958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9451bb0011bcbf1daf2d00410a734f9750c021ad8aebe4d391a64fdb3e1971d1`  
		Last Modified: Wed, 14 Feb 2024 00:42:26 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.6.7-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:8cc763722290d52ec2b1a7fa18c628d2630411b0bbe1a661cac3fb2ec2bb4151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2133754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77fa3a8b17893a35d1023aa52f8adc2684a373d93191eb7ca6260843a1a6b170`

```dockerfile
```

-	Layers:
	-	`sha256:63a9b0ef4a753f8b9fb3fd2346a01b6aa5480cd222052744cf4b000957a1a1b9`  
		Last Modified: Wed, 14 Feb 2024 00:42:26 GMT  
		Size: 2.1 MB (2115791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6f7b5d56798cccc7af9f29454a32b0ef2b633c7c8e51e585db5877186617942`  
		Last Modified: Wed, 14 Feb 2024 00:42:26 GMT  
		Size: 18.0 KB (17963 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.6.7-bookworm` - linux; 386

```console
$ docker pull julia@sha256:33f51106daf2cb9f30fe8d9b9062b7b5f81ee6077ce736da915ca0d0310fb9de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156096437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85a982556a5c23ceeb73b8cbf696d3d6a06acc7aa74109a3eae1a627756648e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 10 Nov 2023 15:26:46 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["bash"]
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 10 Nov 2023 15:26:46 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_VERSION=1.6.7
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.6.7","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.6.7?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f077852809d3df0ff0aaa7a7999f678d46ef0610856b3cdfeb43cfa4f5640b9`  
		Last Modified: Tue, 13 Feb 2024 01:53:50 GMT  
		Size: 5.9 MB (5863266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1f1076a2abdc9cee969fb84b5be03f8fa38280081598bd24a7d3571754d0e8`  
		Last Modified: Tue, 13 Feb 2024 01:53:53 GMT  
		Size: 120.1 MB (120090994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8cc012aa6af202e8c794bdeefa180135dd62b2d847c2de62028bb0d8f7d3ec`  
		Last Modified: Tue, 13 Feb 2024 01:53:50 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.6.7-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:591fbb52b8d270de8a94e59e0b76349486c19676866f93ac08fcbc0723755ff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2130741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9492628cf08b5352cfb403a015a7c43586f5f454e1457e5e00619820fed796b4`

```dockerfile
```

-	Layers:
	-	`sha256:a838468fc0caa024ea0293c369b3c4b3704212fd01d445d6e48389a9fae99d63`  
		Last Modified: Tue, 13 Feb 2024 01:53:50 GMT  
		Size: 2.1 MB (2112654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:195d2faeee1d99524485898b2275f5c342519a2088c7821a5981b3aa95aff7cf`  
		Last Modified: Tue, 13 Feb 2024 01:53:50 GMT  
		Size: 18.1 KB (18087 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.6.7-bullseye`

```console
$ docker pull julia@sha256:e0fddb0b232aa234ec0cd86aa9bed756249f86b3cedf5dabd543b213ccaa399d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.6.7-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:ae93e84f40b527b886c50aa4e778d752a93f67c8eeb5ccc47fbbde8a4b3ad751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.3 MB (156273540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e9a8aa572dcbf8bcbcabc32a448cc737b3fad7cacba953b096e7160f6f57b3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 10 Nov 2023 15:26:46 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["bash"]
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 10 Nov 2023 15:26:46 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_VERSION=1.6.7
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.6.7","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.6.7?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44055ebbad9a840edd272723b88393e077281ccca3a1b698a3d44b26563cae8e`  
		Last Modified: Tue, 13 Feb 2024 01:53:46 GMT  
		Size: 2.4 MB (2426505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f6e5deb2eac362f8750eddaad28bf4f5d4e151edd12382369644f9e8d53834`  
		Last Modified: Tue, 13 Feb 2024 01:53:48 GMT  
		Size: 122.4 MB (122424246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e96350ebccfd7a4233369bfd04632aa48f1b42fe8bc74332302521f0c557d78`  
		Last Modified: Tue, 13 Feb 2024 01:53:46 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.6.7-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:82db38e2c28e78689c893ea49525d25ce922b8cb7a3e4e9e0965c7446d032baa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2354084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c1d7019ada9a32c38a25e9a25c469bb25e8e1aef8f4124b4aec63aea1063660`

```dockerfile
```

-	Layers:
	-	`sha256:9b4bde1258c12fc31e0a0e43a465f3387b238b5ec05a2c1b6736190460b9a5aa`  
		Last Modified: Tue, 13 Feb 2024 01:53:46 GMT  
		Size: 2.3 MB (2336548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:faeb5bdda1ddfe200c6a09badaac3b6663d765788475daa796bea35d8f2cdb62`  
		Last Modified: Tue, 13 Feb 2024 01:53:46 GMT  
		Size: 17.5 KB (17536 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.6.7-bullseye` - linux; arm variant v7

```console
$ docker pull julia@sha256:166a3c80fe18f6af1fb4ee062820e8cc3d13bdfb796bf6a440bd0f74860626ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142077562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3194d7833dbcaa7dce91eda133eb75e4a0e1e9b1f7ce9000e8a51291c7df7044`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 10 Nov 2023 15:26:46 GMT
ADD file:65b9e2efdf2b09faf0d5ea0e2e00984ff3c8cf89b7959287bc6ca54c7772801d in / 
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["bash"]
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 10 Nov 2023 15:26:46 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_VERSION=1.6.7
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.6.7","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.6.7?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4de6a546d77461a35cb9514c6432142adfb72460cf04bac21bd261d66c288476`  
		Last Modified: Wed, 31 Jan 2024 22:49:36 GMT  
		Size: 26.6 MB (26579212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5231778797bc56a4a08ab1f98a7404c0ce93eba8510a46cb8cfa5cc105b33787`  
		Last Modified: Sat, 03 Feb 2024 11:35:00 GMT  
		Size: 2.0 MB (2025850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca298d55f5af2ac1229b547303326aaa61682035cefda0e23a8663fbf4da4a8`  
		Last Modified: Sat, 03 Feb 2024 11:35:03 GMT  
		Size: 113.5 MB (113472127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f863e5ff6e69d1c00d6dd2e5d868f67670607ebe5adf245b4b3a146b4366d209`  
		Last Modified: Sat, 03 Feb 2024 11:35:00 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.6.7-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:e3855ff86bd536f471d2e159ee3d2f9e91aae035551272b3aec98139458885db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2264566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8e365ee64c374ebdbac5392b32bbe79ea9fdc93134ece6269ad3f7837a3e5e5`

```dockerfile
```

-	Layers:
	-	`sha256:383e5a8123f306e0d60e7c11d64b25f830595aa16c73879f60c21a87981b37f3`  
		Last Modified: Sat, 03 Feb 2024 11:35:00 GMT  
		Size: 2.2 MB (2247130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c1413c4451427a6e8345c839f48a9fb1501e8cececcad57338c87c5a0871a0e`  
		Last Modified: Sat, 03 Feb 2024 11:35:00 GMT  
		Size: 17.4 KB (17436 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.6.7-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:f547698892cdc1d19af623341188826eb0edc5b15e132f5f5027e48ab9b14e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148698555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9afba32909e96b304eddd83ab804f6487753adfc8add922f36413c95ec4f46d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 10 Nov 2023 15:26:46 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["bash"]
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 10 Nov 2023 15:26:46 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_VERSION=1.6.7
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.6.7","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.6.7?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1acd381bc5ce074386a44640a70f3d2d53921e7cda7c6386a20616c9fab4cee5`  
		Last Modified: Wed, 14 Feb 2024 00:41:34 GMT  
		Size: 2.4 MB (2415040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c90b692c61af45526b067b1bf1b2ceb13322db12eee47fbe8f1cc1a96d89609`  
		Last Modified: Wed, 14 Feb 2024 00:43:16 GMT  
		Size: 116.2 MB (116212069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1eb6a1cae9a6a5309398434109d4a94bbd1ec71ef01f09ab8a64a211a5b14b`  
		Last Modified: Wed, 14 Feb 2024 00:43:12 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.6.7-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:59551459df38eaacc35fdc3b8cea8f9e26214868c9943218cb196d38b559d13d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2354244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f30befc2b480479913e1a574a4d602ae24fc0d0f1761b1c8212036a7e8a9da3`

```dockerfile
```

-	Layers:
	-	`sha256:578a1641140e2764a9b5b86a0b77b591b42e0ec193255acd1b6cbb1eaad391c1`  
		Last Modified: Wed, 14 Feb 2024 00:43:13 GMT  
		Size: 2.3 MB (2336869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60187de5d671b93e104cc6ce28301c7f9a269b4c44df1f2c1b6adeca6db6e9a8`  
		Last Modified: Wed, 14 Feb 2024 00:43:12 GMT  
		Size: 17.4 KB (17375 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.6.7-bullseye` - linux; 386

```console
$ docker pull julia@sha256:519503c3933ece0eea52e55edfae5f9544474a717d1b9b24f3fde56b8f7c45f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.0 MB (155031210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:146d6c24a377c4bce3621687747a06a0a575aab993166f04da5dbd93236a46cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 10 Nov 2023 15:26:46 GMT
ADD file:9eaee5af136d095dc1dac0ffce0fde09d8f1bd02ff7cb65ee67e00b2a66f34f7 in / 
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["bash"]
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 10 Nov 2023 15:26:46 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_VERSION=1.6.7
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.6.7","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.6.7?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1ac8173b08d16f9f136fb0e3ee39999cef7495f924ecb43f3ca4a4eea267cc88`  
		Last Modified: Tue, 13 Feb 2024 00:44:36 GMT  
		Size: 32.4 MB (32407443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88194674edbd99cb92bce2bf868fbcbfa1f9e3705fd917a20de4f7c9348380f8`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 2.5 MB (2533059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3772b84a9011053ab51ee0620e3020ffac7503a8d7ec421bd5993500ed179d`  
		Last Modified: Tue, 13 Feb 2024 01:53:58 GMT  
		Size: 120.1 MB (120090340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7caf8fda699f4879be705ad5ba0cc80939ac60a77f94801a05d3adc6710e1b`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.6.7-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:b1997b9cb6650ef1915f3585b569cf8f35f99859600a6f78e7f279bff3869a6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2351279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecccd630382a36d25e217634cff89737577676dc09de2fb845d9b9d28b1a8e3c`

```dockerfile
```

-	Layers:
	-	`sha256:5ec454dc25b4c298a3a1cf315339c2bf11d6b455a694e218fb8b26782e967393`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 2.3 MB (2333764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec66f549b1093d1f19ee98fb6f4a133764488bec8ef952548f7b315aac4b4633`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 17.5 KB (17515 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.6.7-windowsservercore`

```console
$ docker pull julia@sha256:c2f87c3d76e487009bdca4540789a155dbb7b336389b817e215cc3c02f20e999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `julia:1.6.7-windowsservercore` - windows version 10.0.20348.2227; amd64

```console
$ docker pull julia@sha256:aacbbc8940601c0e5596931fa9d41cce28ab1fa2c31c78c1d116e219483534c7
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2034764054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:543f707ae687e7e690271d7fe6f8b11b7c62dc6f786e23fee7dadc2b52c6351e`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Thu, 11 Jan 2024 00:08:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:08:01 GMT
ENV JULIA_VERSION=1.6.7
# Thu, 11 Jan 2024 00:08:02 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Thu, 11 Jan 2024 00:08:02 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Thu, 11 Jan 2024 00:08:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:08:50 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ec27c9842b8e899a5278c55aa21d2cf14e62ae5b8dbc8ef21ffe38683f694d`  
		Last Modified: Thu, 11 Jan 2024 00:08:56 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12f858d296dd90c13c42516bcc60fae65f52207d2846a54ad3e3c059b87bf85`  
		Last Modified: Thu, 11 Jan 2024 00:08:54 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37065f76f4d697c310167b0cf169601492542ffeb7174129d6077ec8af74ff49`  
		Last Modified: Thu, 11 Jan 2024 00:08:54 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b334853e6c04835809903c081d10c7faa8ee0d9d6d3684d89e8d6954e2725c5`  
		Last Modified: Thu, 11 Jan 2024 00:08:54 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109a7946e539e9a6238d5492f541cd7ce6b55b428fdf1d34f9ead65ac74bb682`  
		Last Modified: Thu, 11 Jan 2024 00:09:12 GMT  
		Size: 134.5 MB (134544929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35917c15fff017c85a175e4c462c3fc80c624510736cf63a746358851e462b7f`  
		Last Modified: Thu, 11 Jan 2024 00:08:54 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6.7-windowsservercore` - windows version 10.0.17763.5329; amd64

```console
$ docker pull julia@sha256:09f0a64aa6af42e12b9c0667122016bbda84151ebbc217b59fc24aa875e3e953
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2204271920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2770e04b2d617a0710f509eaa78ee9e3db8e0c4742f63c90e174a5277fb3889`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:04:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:04:59 GMT
ENV JULIA_VERSION=1.6.7
# Thu, 11 Jan 2024 00:05:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Thu, 11 Jan 2024 00:05:01 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Thu, 11 Jan 2024 00:06:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:06:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018567616bba50c617270b645f6f9f5eeffc82add802ee321a43b1cbcabf047d`  
		Last Modified: Thu, 11 Jan 2024 00:06:29 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f16287f2b89a420c3c6ff9e6b119a9bac0bca4711c2c38160c6725a076af14a`  
		Last Modified: Thu, 11 Jan 2024 00:06:27 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b9460df90a5ea657a924cb2e8e06f9d231da0255adfe2727c85142c3b9acbff`  
		Last Modified: Thu, 11 Jan 2024 00:06:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2307766466bf7a0f3659aed4269cb3895dde01f7f7d2eb6bf4a40a5893ac05b`  
		Last Modified: Thu, 11 Jan 2024 00:06:27 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaceb21bd3ac6440c397b6e7b9de7788c1019a0f1ed396375f20819fb2e82d1`  
		Last Modified: Thu, 11 Jan 2024 00:06:45 GMT  
		Size: 134.5 MB (134542902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4ebe971903a073c38f33636a0c5c3435c9abef3f9e10437c9b35e51c33e674`  
		Last Modified: Thu, 11 Jan 2024 00:06:27 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6.7-windowsservercore-1809`

```console
$ docker pull julia@sha256:e6acba1d8d740dd47c572f3fe4637b29247fe6a6924c7ea2d050f09f4747a2e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `julia:1.6.7-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull julia@sha256:09f0a64aa6af42e12b9c0667122016bbda84151ebbc217b59fc24aa875e3e953
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2204271920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2770e04b2d617a0710f509eaa78ee9e3db8e0c4742f63c90e174a5277fb3889`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:04:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:04:59 GMT
ENV JULIA_VERSION=1.6.7
# Thu, 11 Jan 2024 00:05:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Thu, 11 Jan 2024 00:05:01 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Thu, 11 Jan 2024 00:06:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:06:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018567616bba50c617270b645f6f9f5eeffc82add802ee321a43b1cbcabf047d`  
		Last Modified: Thu, 11 Jan 2024 00:06:29 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f16287f2b89a420c3c6ff9e6b119a9bac0bca4711c2c38160c6725a076af14a`  
		Last Modified: Thu, 11 Jan 2024 00:06:27 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b9460df90a5ea657a924cb2e8e06f9d231da0255adfe2727c85142c3b9acbff`  
		Last Modified: Thu, 11 Jan 2024 00:06:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2307766466bf7a0f3659aed4269cb3895dde01f7f7d2eb6bf4a40a5893ac05b`  
		Last Modified: Thu, 11 Jan 2024 00:06:27 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaceb21bd3ac6440c397b6e7b9de7788c1019a0f1ed396375f20819fb2e82d1`  
		Last Modified: Thu, 11 Jan 2024 00:06:45 GMT  
		Size: 134.5 MB (134542902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4ebe971903a073c38f33636a0c5c3435c9abef3f9e10437c9b35e51c33e674`  
		Last Modified: Thu, 11 Jan 2024 00:06:27 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6.7-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:afbab72fbecd773fc4aba01df3cf9a781228c934da8685c8a59704922a00edb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `julia:1.6.7-windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull julia@sha256:aacbbc8940601c0e5596931fa9d41cce28ab1fa2c31c78c1d116e219483534c7
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2034764054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:543f707ae687e7e690271d7fe6f8b11b7c62dc6f786e23fee7dadc2b52c6351e`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Thu, 11 Jan 2024 00:08:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:08:01 GMT
ENV JULIA_VERSION=1.6.7
# Thu, 11 Jan 2024 00:08:02 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Thu, 11 Jan 2024 00:08:02 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Thu, 11 Jan 2024 00:08:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:08:50 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ec27c9842b8e899a5278c55aa21d2cf14e62ae5b8dbc8ef21ffe38683f694d`  
		Last Modified: Thu, 11 Jan 2024 00:08:56 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12f858d296dd90c13c42516bcc60fae65f52207d2846a54ad3e3c059b87bf85`  
		Last Modified: Thu, 11 Jan 2024 00:08:54 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37065f76f4d697c310167b0cf169601492542ffeb7174129d6077ec8af74ff49`  
		Last Modified: Thu, 11 Jan 2024 00:08:54 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b334853e6c04835809903c081d10c7faa8ee0d9d6d3684d89e8d6954e2725c5`  
		Last Modified: Thu, 11 Jan 2024 00:08:54 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109a7946e539e9a6238d5492f541cd7ce6b55b428fdf1d34f9ead65ac74bb682`  
		Last Modified: Thu, 11 Jan 2024 00:09:12 GMT  
		Size: 134.5 MB (134544929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35917c15fff017c85a175e4c462c3fc80c624510736cf63a746358851e462b7f`  
		Last Modified: Thu, 11 Jan 2024 00:08:54 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:alpine`

```console
$ docker pull julia@sha256:15acea4c3855874b1349caf0600c7da2b05033ccfe67d0a8693edf814d1007e8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:alpine` - linux; amd64

```console
$ docker pull julia@sha256:54a01c7689d514bf51a3494279a6877120729ed258de377f503d4782fca53bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176683112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432f75cca29ad8d3247b11295ee97b5a12c070431990e6180904f99400965b39`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["/bin/sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.0-musl-x86_64.tar.gz'; 			sha256='da8a9e0cf31eddd776276321802b9744acf5b8ce0171854b3e9d6394f656f9a2'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d8037af8d1d0f5fa4e82d16f39e0b5b2d7bb3071eeca07feddb80d63a9f084`  
		Last Modified: Sat, 27 Jan 2024 00:53:32 GMT  
		Size: 173.3 MB (173274017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534faee11eeb72a12ad121faf92d04078fb81e27ca029a61603381e7bfdade5c`  
		Last Modified: Sat, 27 Jan 2024 00:53:28 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:alpine` - unknown; unknown

```console
$ docker pull julia@sha256:4986f231ec2d9910a78844ccfbbedb86e0c958c6201d42a9a98f2e9208690dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.7 KB (83724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d769d8b51235a19931eb01c03a4bd6662cd2d79ec929b72c3ffd574289061c2a`

```dockerfile
```

-	Layers:
	-	`sha256:ba24d43b9b3ea2e4c533f1d19a970a9e97e8d6fdd95a182466235e35e952196e`  
		Last Modified: Sat, 27 Jan 2024 00:53:28 GMT  
		Size: 69.0 KB (69026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abe1763c27a7fb5692262541e30b12b927086a838ced1e6191ae3bdba7e05191`  
		Last Modified: Sat, 27 Jan 2024 00:53:28 GMT  
		Size: 14.7 KB (14698 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:alpine3.18`

```console
$ docker pull julia@sha256:77a977b5edcfe0878250b81503abbe31f1425e64a0f12e1ada4d51b1da34758c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:alpine3.18` - linux; amd64

```console
$ docker pull julia@sha256:5299d783ae55d8ef632b9cc263458d66a810a4de77a03ffae4e7fa820264aa53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176676774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee49bd257b2df90a18d0154e828326a5fcba99b347173d2169fe13bcd43dff0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["/bin/sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.0-musl-x86_64.tar.gz'; 			sha256='da8a9e0cf31eddd776276321802b9744acf5b8ce0171854b3e9d6394f656f9a2'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=alpine&os_version=3.18"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5204fc615595fd1ad835b0750c5fdb927818512d88052aef7e3850c09dd45475`  
		Last Modified: Sat, 27 Jan 2024 00:53:33 GMT  
		Size: 173.3 MB (173273866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3bd7244621863d2bbcbbe233abec587e6b376a86cab3eaec7803f2556e535f`  
		Last Modified: Sat, 27 Jan 2024 00:53:29 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:alpine3.18` - unknown; unknown

```console
$ docker pull julia@sha256:da0ca027e598e9773b125a066c844f5cefc1ecbbfb387e5b7661abd53bd31fe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 KB (80746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c093cd0eedbfc6980a82434ffc3879914906fc76b8f084df18d5c9012ffdb2aa`

```dockerfile
```

-	Layers:
	-	`sha256:58ec49d3d0285541a48ea975d3b7fdda895fc33f2c2d93c8933a42c1a3651f1a`  
		Last Modified: Sat, 27 Jan 2024 00:53:29 GMT  
		Size: 67.3 KB (67260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:187a1d23ed3a8d36572659404c674c1615b777fd9041abe5246a10eb10691ae7`  
		Last Modified: Sat, 27 Jan 2024 00:53:29 GMT  
		Size: 13.5 KB (13486 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:alpine3.19`

```console
$ docker pull julia@sha256:15acea4c3855874b1349caf0600c7da2b05033ccfe67d0a8693edf814d1007e8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:alpine3.19` - linux; amd64

```console
$ docker pull julia@sha256:54a01c7689d514bf51a3494279a6877120729ed258de377f503d4782fca53bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176683112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432f75cca29ad8d3247b11295ee97b5a12c070431990e6180904f99400965b39`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["/bin/sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.0-musl-x86_64.tar.gz'; 			sha256='da8a9e0cf31eddd776276321802b9744acf5b8ce0171854b3e9d6394f656f9a2'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d8037af8d1d0f5fa4e82d16f39e0b5b2d7bb3071eeca07feddb80d63a9f084`  
		Last Modified: Sat, 27 Jan 2024 00:53:32 GMT  
		Size: 173.3 MB (173274017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534faee11eeb72a12ad121faf92d04078fb81e27ca029a61603381e7bfdade5c`  
		Last Modified: Sat, 27 Jan 2024 00:53:28 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:alpine3.19` - unknown; unknown

```console
$ docker pull julia@sha256:4986f231ec2d9910a78844ccfbbedb86e0c958c6201d42a9a98f2e9208690dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.7 KB (83724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d769d8b51235a19931eb01c03a4bd6662cd2d79ec929b72c3ffd574289061c2a`

```dockerfile
```

-	Layers:
	-	`sha256:ba24d43b9b3ea2e4c533f1d19a970a9e97e8d6fdd95a182466235e35e952196e`  
		Last Modified: Sat, 27 Jan 2024 00:53:28 GMT  
		Size: 69.0 KB (69026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abe1763c27a7fb5692262541e30b12b927086a838ced1e6191ae3bdba7e05191`  
		Last Modified: Sat, 27 Jan 2024 00:53:28 GMT  
		Size: 14.7 KB (14698 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:bookworm`

```console
$ docker pull julia@sha256:ae0f50e0d812f1537df24444125ca4b894e0e4a0e293b897b9ada6726f0ac007
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
$ docker pull julia@sha256:c581649ac221ebfbea9798a3bd66dfb0ba0dd44ba20ff5262d3c8bb93a759346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.9 MB (205909072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b184ca25c5acda81d0dc2e137ccf411bdd8e9f61fdd835d4bd55637d23b835`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad1c4eb009e797d65c1acfac69cd12c8f9060f29f760108f933027f2caab9c3`  
		Last Modified: Tue, 13 Feb 2024 01:53:54 GMT  
		Size: 5.7 MB (5707977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef8b6ee7f7fb149365afb062c086c37b5b314813fc6ec90095b002f5a925f0b`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 171.1 MB (171076635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d82177bdd251b5f04cc2ba1e5fd4efbafdbd4770a176a106cc21f400dbc05a`  
		Last Modified: Tue, 13 Feb 2024 01:53:54 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:3b5ca3771866b183000dca0a20d1bd2cb30d18b3a75d2ff32ac5cacaf423ef41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2158401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1bf8696406f25674e86fbc2d37065b3233c46aeb745f75fb02a0207775ca9a`

```dockerfile
```

-	Layers:
	-	`sha256:0884c94ffa8afd7175e4fdf92aa18f71815867215f0cde964240ba45b4f94154`  
		Last Modified: Tue, 13 Feb 2024 01:53:54 GMT  
		Size: 2.1 MB (2139045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:348b64f895c758148af65a9d8d6cf1581a93e955b08d7c118bee6923d2672bda`  
		Last Modified: Tue, 13 Feb 2024 01:53:54 GMT  
		Size: 19.4 KB (19356 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:c7b50eb125b7d60c63329a2c13798bc0c6e71611739c313a8ac466b505e9daab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199068374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc9cfd7eb49e87c970aa3df455f5951bd13608a351ad60fa41258f33c872dad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b14e605bd6638a1976eeb8d1cde59556a1f77295bac46d1669a9e27e6cd0ad6`  
		Last Modified: Wed, 14 Feb 2024 00:40:29 GMT  
		Size: 5.5 MB (5533149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d7d4913392d7182590a28188bd4fa882d0ed53f36bf9d49c1b5dfd74dda0ce`  
		Last Modified: Wed, 14 Feb 2024 00:40:32 GMT  
		Size: 164.4 MB (164378492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c05a2fc2483ea3c18ac5829c7ca9c7c9fd40204cb09b4ace74a3c02cb27dbe9`  
		Last Modified: Wed, 14 Feb 2024 00:40:28 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:7812cc45c880626d2dfa14638dfc0dcca6d09a54e1b49abf8d917a8f8a6fd61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2157622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d96f6d9b1c89aaf182d67e03efcae208a6f69ae643a004df4c24d36a84b881f`

```dockerfile
```

-	Layers:
	-	`sha256:ffca818dcaa241a02e65213ba00b90e138a6c248aaa839bb326ddf81d27472f1`  
		Last Modified: Wed, 14 Feb 2024 00:40:29 GMT  
		Size: 2.1 MB (2138415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7b32281e96ad074af12b3d2e1fec978b2b8afb5106ab0eeb89189cedc13c81d`  
		Last Modified: Wed, 14 Feb 2024 00:40:29 GMT  
		Size: 19.2 KB (19207 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; 386

```console
$ docker pull julia@sha256:ed5dae7c246f3779da0892e59fefc8a2a06c1b0418c75cc66df890b64fbd5d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192476013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266a487238b5f50dc9dd3bc262639f4da7f6d7b6194a3f48742cf1725df03675`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adcfe329152d3631bed65ca802c4d591cf2466ececc127b4689e12fd044b6dd9`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 5.9 MB (5863232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7f556d75a67e2c4d02467097026cac3136c670701b05d1fe37c2209b150c66`  
		Last Modified: Tue, 13 Feb 2024 01:53:58 GMT  
		Size: 156.5 MB (156470603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee51a4a243b601cbdaea50eb3df43c6297660d3956259740ebcbb63126d2d0a`  
		Last Modified: Tue, 13 Feb 2024 01:53:54 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:98bc5d459492dc920f2634c7d2a39252f464f40045e8ee9bb9a967df561e7fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2155528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741936c96e550374e6be8d4320cd5b8e3cf1b315e382afac934f7edfc2236eb3`

```dockerfile
```

-	Layers:
	-	`sha256:53aa4312033ace4a7cf6f547e9085d8bd6890df5b2615d784fc182399ed92297`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 2.1 MB (2136223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3060f20bd073e1f89280df62e40daa82ac66677706d6628b0e7ce70250402b51`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 19.3 KB (19305 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:42518fad4d8a20363e408d6bf3ce4259a1203bc1f3a1720ede05055daf233cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.3 MB (193349040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc361617127c03f5ef43a89da3fa93390c1213068a6e940b721330dc4e63a12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:b65bdf3d9277efbf6bbf8bf0121f92bdcd342ed0c4f49f1cee3b91adafacd76c in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b1cce6d9947985e4270ac998aa258401bc5deca94d504040a14f9f3c47258d68`  
		Last Modified: Tue, 13 Feb 2024 00:43:56 GMT  
		Size: 33.1 MB (33118908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a48b566372cb4fa0fec129e803c39a28de529b9736fd03a42344641249c1fc`  
		Last Modified: Tue, 13 Feb 2024 21:54:44 GMT  
		Size: 6.2 MB (6239799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85e6dfe440366f653bf664315e491fe0cb2bb189428018fbcf657460fbbc3fa`  
		Last Modified: Tue, 13 Feb 2024 21:54:47 GMT  
		Size: 154.0 MB (153989961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6306b805ea4661e164d23cfd0d8dfae9d27c498477a790d3351d0f6ecc3e5fd`  
		Last Modified: Tue, 13 Feb 2024 21:54:43 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:8ed461f46641215c54d31c67c06954851c85f63b1d2b4eebe9351ecff9289da9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2161862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286b8e56e5b1f465b474b30b2fe8512b0c2238bef520a8bd95c4e5e31b59df2c`

```dockerfile
```

-	Layers:
	-	`sha256:9da0b3fffb06b598b8c17e331a4e70d4e6b54c5bfad5a40d4e88a16d3966ab41`  
		Last Modified: Tue, 13 Feb 2024 21:54:43 GMT  
		Size: 2.1 MB (2142609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbfe360df232fd616240d3f8aae495b7a956d6a7383dcdf4dc8ae56cd7d319c2`  
		Last Modified: Tue, 13 Feb 2024 21:54:43 GMT  
		Size: 19.3 KB (19253 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:bullseye`

```console
$ docker pull julia@sha256:f6dd1793015df42b577c0375b98514ba7979171f5957bb0e475aa3539ef21d5d
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

### `julia:bullseye` - linux; amd64

```console
$ docker pull julia@sha256:8d384ae00c7c02cbee899728190fcdd1faca693ec80fed6d734c76a84922a118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 MB (204925804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19950a8b05c384b4f92d751f4f10a98e63aa069ead4d5cf9186b030c920da3a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f3f6d4871c74f7b63e34b697a9aaefa8835f1889dc6903866338a86317002e`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 2.4 MB (2426534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba72295cd998aea9729c2a415acf7f007a528c2b4d6f1c34387bb92d9bac746`  
		Last Modified: Tue, 13 Feb 2024 01:53:58 GMT  
		Size: 171.1 MB (171076476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d0425419406b5a1143dff3543f91ff035c7d0ecb9bf0774e64e01554e02e20`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:8273a9fdda9b316a362eeb3ea1e578ee9092b278a30a718754a7c3a8deacd3e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04952d04716e6ab86f7cf6f5e35bd7873721540b5380dd2811279304f811d7f4`

```dockerfile
```

-	Layers:
	-	`sha256:432180086c941804e7ee5fcf6bd251520e95f0fdb359e58e157794fe17baa0b4`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 2.4 MB (2359551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:870a84f47d45ed4bb0321a5cc4914f58d0ee37c40ea0d352c1b840eaa8d48cca`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 18.2 KB (18186 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:5487dbd9e86ea6dfdde1e83477c820ef9096cbd52e19dcc574b6fd9efb76b2ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.9 MB (196864925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80daa6ec8fc78a3eec97067ae5b96e344d99367cccefba598286c51b1386fdf0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1acd381bc5ce074386a44640a70f3d2d53921e7cda7c6386a20616c9fab4cee5`  
		Last Modified: Wed, 14 Feb 2024 00:41:34 GMT  
		Size: 2.4 MB (2415040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520a7f557218cd3b5ef3f4ddd5afcca8d80438c186a9bf2521eda165facd2c91`  
		Last Modified: Wed, 14 Feb 2024 00:41:38 GMT  
		Size: 164.4 MB (164378442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:268a60e13473050784334fa5d0cc23da2209b45f3251f0133c2c05c309d0b752`  
		Last Modified: Wed, 14 Feb 2024 00:41:33 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:f8bb44f08113f3d1137034416ccf2f473631f08424eb97007061de4ac057ae2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2376931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:951d6f2d9e6a3d58bcd7de98a60c4417e42eeafb974b36e71f6fb0760357a357`

```dockerfile
```

-	Layers:
	-	`sha256:7beff45e48bb073460b5214a082784914cd78b5c8864627f675670dff6784190`  
		Last Modified: Wed, 14 Feb 2024 00:41:34 GMT  
		Size: 2.4 MB (2358903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2687ab055e0cc2332a76ad9df388d45043b631992252746a3b6d1260836fc41`  
		Last Modified: Wed, 14 Feb 2024 00:41:34 GMT  
		Size: 18.0 KB (18028 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bullseye` - linux; 386

```console
$ docker pull julia@sha256:3348a4e15f9eb821e27b64f594aee5b549605b9a02ce2d81bf0296660348dccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191411992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34cc23d0f384f592a3f59a3d676eb76d72ea43b54725d5f8e0baeb644aebdffb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:9eaee5af136d095dc1dac0ffce0fde09d8f1bd02ff7cb65ee67e00b2a66f34f7 in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1ac8173b08d16f9f136fb0e3ee39999cef7495f924ecb43f3ca4a4eea267cc88`  
		Last Modified: Tue, 13 Feb 2024 00:44:36 GMT  
		Size: 32.4 MB (32407443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf492369ec4d56d2010213bf0c01a1d0be40c950eda27da51921ed8c2a1bc09`  
		Last Modified: Tue, 13 Feb 2024 01:53:53 GMT  
		Size: 2.5 MB (2533067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7d0f5baeea89d7b49c54cc577eab3867247693f466f98b3cc4f2399efcb0af`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 156.5 MB (156471113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6be2aecc9dc90a8f90619365daf78c2fc8f2c67056592b5b10683e9b84c892`  
		Last Modified: Tue, 13 Feb 2024 01:53:53 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:8016124e8b1742e9b8063df61bae834e255e72ef863ed54fde680195b00a6e09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2374912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9820be04702fdac240a66ebb9fed36ff9a01b291501d69df9966aaa79cbb048`

```dockerfile
```

-	Layers:
	-	`sha256:b5b0fa0ccbf3afd955632b36296386d1988c6a60b808e7101b4b3f9320935cd2`  
		Last Modified: Tue, 13 Feb 2024 01:53:53 GMT  
		Size: 2.4 MB (2356757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:427416a00deb6fc64dea6ac42ea75526fa410b61d0f98ed7c269e848697a670b`  
		Last Modified: Tue, 13 Feb 2024 01:53:53 GMT  
		Size: 18.2 KB (18155 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bullseye` - linux; ppc64le

```console
$ docker pull julia@sha256:34e38bddb83d3e554661ccd943af43cdb864af337b665e80d319d17641dcae38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.9 MB (191918984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce2e008edde3927a13f00754ee8f8a138c1cccfbf871fbecc2c26aa365977fee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:f8e53a63f5fbfb32b4bac66dc2b16f2e2d101e5feb6cd9e3b6d3065fb8aee14d in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5c87ba6a2e42f083a6cfdea0d3b1b3bc977a5065ff0087fdbf4fc8dbc7982a38`  
		Last Modified: Tue, 13 Feb 2024 00:44:50 GMT  
		Size: 35.3 MB (35297799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc406362a4b5aed4760caff7c4bc06a04cb2bd3834a923f056a5baf70eb0d7ff`  
		Last Modified: Tue, 13 Feb 2024 21:56:31 GMT  
		Size: 2.6 MB (2629991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278b4e0551a3587b5d022b566e56d527b968803375aa151bdd2dc6d30b7c7813`  
		Last Modified: Tue, 13 Feb 2024 21:56:34 GMT  
		Size: 154.0 MB (153990822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a158664e796ca3ee0566bb6b7e2b79e13c3161c9f36f6dadb04bf7cdcbb6e58`  
		Last Modified: Tue, 13 Feb 2024 21:56:30 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:074faa55f685aff95e390f40bbece0962016efb2de45e76932ad7ec77379eb75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adae430aa8a2857fe05d29dfd22203f96e4ba41334491bf64c9bcf168e2689ce`

```dockerfile
```

-	Layers:
	-	`sha256:a3834b7b363b094f8ccc42c1d8c1266c29a4d88ab2002bc4a6d745aef0871e7b`  
		Last Modified: Tue, 13 Feb 2024 21:56:30 GMT  
		Size: 2.4 MB (2363081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22fd53c802c699b2d4eec0a68f896ffad71210add2b28509849ee2d177075647`  
		Last Modified: Tue, 13 Feb 2024 21:56:30 GMT  
		Size: 18.1 KB (18059 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:latest`

```console
$ docker pull julia@sha256:564460379e4782890dbfe5f073481eceb044b96cefb69f45805f9901fee5a747
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
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `julia:latest` - linux; amd64

```console
$ docker pull julia@sha256:c581649ac221ebfbea9798a3bd66dfb0ba0dd44ba20ff5262d3c8bb93a759346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.9 MB (205909072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b184ca25c5acda81d0dc2e137ccf411bdd8e9f61fdd835d4bd55637d23b835`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad1c4eb009e797d65c1acfac69cd12c8f9060f29f760108f933027f2caab9c3`  
		Last Modified: Tue, 13 Feb 2024 01:53:54 GMT  
		Size: 5.7 MB (5707977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef8b6ee7f7fb149365afb062c086c37b5b314813fc6ec90095b002f5a925f0b`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 171.1 MB (171076635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d82177bdd251b5f04cc2ba1e5fd4efbafdbd4770a176a106cc21f400dbc05a`  
		Last Modified: Tue, 13 Feb 2024 01:53:54 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:3b5ca3771866b183000dca0a20d1bd2cb30d18b3a75d2ff32ac5cacaf423ef41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2158401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1bf8696406f25674e86fbc2d37065b3233c46aeb745f75fb02a0207775ca9a`

```dockerfile
```

-	Layers:
	-	`sha256:0884c94ffa8afd7175e4fdf92aa18f71815867215f0cde964240ba45b4f94154`  
		Last Modified: Tue, 13 Feb 2024 01:53:54 GMT  
		Size: 2.1 MB (2139045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:348b64f895c758148af65a9d8d6cf1581a93e955b08d7c118bee6923d2672bda`  
		Last Modified: Tue, 13 Feb 2024 01:53:54 GMT  
		Size: 19.4 KB (19356 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:c7b50eb125b7d60c63329a2c13798bc0c6e71611739c313a8ac466b505e9daab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199068374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc9cfd7eb49e87c970aa3df455f5951bd13608a351ad60fa41258f33c872dad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b14e605bd6638a1976eeb8d1cde59556a1f77295bac46d1669a9e27e6cd0ad6`  
		Last Modified: Wed, 14 Feb 2024 00:40:29 GMT  
		Size: 5.5 MB (5533149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d7d4913392d7182590a28188bd4fa882d0ed53f36bf9d49c1b5dfd74dda0ce`  
		Last Modified: Wed, 14 Feb 2024 00:40:32 GMT  
		Size: 164.4 MB (164378492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c05a2fc2483ea3c18ac5829c7ca9c7c9fd40204cb09b4ace74a3c02cb27dbe9`  
		Last Modified: Wed, 14 Feb 2024 00:40:28 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:7812cc45c880626d2dfa14638dfc0dcca6d09a54e1b49abf8d917a8f8a6fd61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2157622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d96f6d9b1c89aaf182d67e03efcae208a6f69ae643a004df4c24d36a84b881f`

```dockerfile
```

-	Layers:
	-	`sha256:ffca818dcaa241a02e65213ba00b90e138a6c248aaa839bb326ddf81d27472f1`  
		Last Modified: Wed, 14 Feb 2024 00:40:29 GMT  
		Size: 2.1 MB (2138415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7b32281e96ad074af12b3d2e1fec978b2b8afb5106ab0eeb89189cedc13c81d`  
		Last Modified: Wed, 14 Feb 2024 00:40:29 GMT  
		Size: 19.2 KB (19207 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; 386

```console
$ docker pull julia@sha256:ed5dae7c246f3779da0892e59fefc8a2a06c1b0418c75cc66df890b64fbd5d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192476013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266a487238b5f50dc9dd3bc262639f4da7f6d7b6194a3f48742cf1725df03675`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adcfe329152d3631bed65ca802c4d591cf2466ececc127b4689e12fd044b6dd9`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 5.9 MB (5863232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7f556d75a67e2c4d02467097026cac3136c670701b05d1fe37c2209b150c66`  
		Last Modified: Tue, 13 Feb 2024 01:53:58 GMT  
		Size: 156.5 MB (156470603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee51a4a243b601cbdaea50eb3df43c6297660d3956259740ebcbb63126d2d0a`  
		Last Modified: Tue, 13 Feb 2024 01:53:54 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:98bc5d459492dc920f2634c7d2a39252f464f40045e8ee9bb9a967df561e7fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2155528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741936c96e550374e6be8d4320cd5b8e3cf1b315e382afac934f7edfc2236eb3`

```dockerfile
```

-	Layers:
	-	`sha256:53aa4312033ace4a7cf6f547e9085d8bd6890df5b2615d784fc182399ed92297`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 2.1 MB (2136223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3060f20bd073e1f89280df62e40daa82ac66677706d6628b0e7ce70250402b51`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 19.3 KB (19305 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; ppc64le

```console
$ docker pull julia@sha256:42518fad4d8a20363e408d6bf3ce4259a1203bc1f3a1720ede05055daf233cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.3 MB (193349040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc361617127c03f5ef43a89da3fa93390c1213068a6e940b721330dc4e63a12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:b65bdf3d9277efbf6bbf8bf0121f92bdcd342ed0c4f49f1cee3b91adafacd76c in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b1cce6d9947985e4270ac998aa258401bc5deca94d504040a14f9f3c47258d68`  
		Last Modified: Tue, 13 Feb 2024 00:43:56 GMT  
		Size: 33.1 MB (33118908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a48b566372cb4fa0fec129e803c39a28de529b9736fd03a42344641249c1fc`  
		Last Modified: Tue, 13 Feb 2024 21:54:44 GMT  
		Size: 6.2 MB (6239799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85e6dfe440366f653bf664315e491fe0cb2bb189428018fbcf657460fbbc3fa`  
		Last Modified: Tue, 13 Feb 2024 21:54:47 GMT  
		Size: 154.0 MB (153989961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6306b805ea4661e164d23cfd0d8dfae9d27c498477a790d3351d0f6ecc3e5fd`  
		Last Modified: Tue, 13 Feb 2024 21:54:43 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:8ed461f46641215c54d31c67c06954851c85f63b1d2b4eebe9351ecff9289da9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2161862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286b8e56e5b1f465b474b30b2fe8512b0c2238bef520a8bd95c4e5e31b59df2c`

```dockerfile
```

-	Layers:
	-	`sha256:9da0b3fffb06b598b8c17e331a4e70d4e6b54c5bfad5a40d4e88a16d3966ab41`  
		Last Modified: Tue, 13 Feb 2024 21:54:43 GMT  
		Size: 2.1 MB (2142609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbfe360df232fd616240d3f8aae495b7a956d6a7383dcdf4dc8ae56cd7d319c2`  
		Last Modified: Tue, 13 Feb 2024 21:54:43 GMT  
		Size: 19.3 KB (19253 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - windows version 10.0.20348.2227; amd64

```console
$ docker pull julia@sha256:795c32c108c365c2480a69a195c9a7e377678d314eefe72f64c230c9178355af
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2083272778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe626ae4264c3793e3f2752abc204a549a77a114b9658003d2cda440332150c6`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Thu, 11 Jan 2024 00:02:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:02:52 GMT
ENV JULIA_VERSION=1.10.0
# Thu, 11 Jan 2024 00:02:53 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.0-win64.exe
# Thu, 11 Jan 2024 00:02:54 GMT
ENV JULIA_SHA256=f58aaa631748a5b0389586f3a3b7a081a2a6ac219a5a73a501ac61c0d99daebd
# Thu, 11 Jan 2024 00:04:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:04:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c4a7e196fc6ca93a61a3bbf497fb2b0eca327aa5cf473b95639f61b03c7c1d7`  
		Last Modified: Thu, 11 Jan 2024 00:04:09 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9346ba0550e4beb52f6dad09e1fa6fcd503e75c3df053e5648a54d6dfa7f05`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d7e35a894e972ab63511466519f9a4136a6144e7dbbd6e622be148046ddbaf`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e808d436d368c0aa304f09221c040769d471ae77d9fc07a9bad5a4eff093923`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86dd2e2e2c87845e244df41b72633372b4b9795242f069b3ab2ccbc728756ce8`  
		Last Modified: Thu, 11 Jan 2024 00:04:32 GMT  
		Size: 183.1 MB (183053648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c2cf5808cd6dced23f08a2d0921f88eae3754821b91d2df3decb5d5c8638a6`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.17763.5329; amd64

```console
$ docker pull julia@sha256:465739c99dd446c2698ee1f7151fc4f82c353749d9bc6b828a0e5e1db645c233
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2252827649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e690842a775a28bffae7fca39b8fa765ab792fabd7d6883bbc561866e2726e`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:03:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:03:43 GMT
ENV JULIA_VERSION=1.10.0
# Thu, 11 Jan 2024 00:03:44 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.0-win64.exe
# Thu, 11 Jan 2024 00:03:44 GMT
ENV JULIA_SHA256=f58aaa631748a5b0389586f3a3b7a081a2a6ac219a5a73a501ac61c0d99daebd
# Thu, 11 Jan 2024 00:05:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:05:27 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9e301d4f97511dcb9f3216268f983f8b8a38f59f6f47d7fcfa6c74bd89340c`  
		Last Modified: Thu, 11 Jan 2024 00:05:35 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15e9906d04250bd67cb869011a80e67292f17770b36865f9ce3b3f07765278f`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6305ccc6bbbc63d35ea2541315eff9b40ff82631ddc08cf97bae6597d416e35d`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fead423ba6e49e59afeb0485520bcfc1ca1f5231bc0104438c670c75c56d67a`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de60c693e3b77965993cdcd8ccef1ce49bbfd61e59f5e5f85a7b950645ce499b`  
		Last Modified: Thu, 11 Jan 2024 00:05:58 GMT  
		Size: 183.1 MB (183098483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ab8928320d6137aceb0a714f2cc037f1c072f50385773b2f6f1d39368da3fc`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore`

```console
$ docker pull julia@sha256:e0173a4d8892b7b6234c3d97cc83366460fefb0737c3333da0fda52b9f2fe0c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `julia:windowsservercore` - windows version 10.0.20348.2227; amd64

```console
$ docker pull julia@sha256:795c32c108c365c2480a69a195c9a7e377678d314eefe72f64c230c9178355af
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2083272778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe626ae4264c3793e3f2752abc204a549a77a114b9658003d2cda440332150c6`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Thu, 11 Jan 2024 00:02:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:02:52 GMT
ENV JULIA_VERSION=1.10.0
# Thu, 11 Jan 2024 00:02:53 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.0-win64.exe
# Thu, 11 Jan 2024 00:02:54 GMT
ENV JULIA_SHA256=f58aaa631748a5b0389586f3a3b7a081a2a6ac219a5a73a501ac61c0d99daebd
# Thu, 11 Jan 2024 00:04:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:04:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c4a7e196fc6ca93a61a3bbf497fb2b0eca327aa5cf473b95639f61b03c7c1d7`  
		Last Modified: Thu, 11 Jan 2024 00:04:09 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9346ba0550e4beb52f6dad09e1fa6fcd503e75c3df053e5648a54d6dfa7f05`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d7e35a894e972ab63511466519f9a4136a6144e7dbbd6e622be148046ddbaf`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e808d436d368c0aa304f09221c040769d471ae77d9fc07a9bad5a4eff093923`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86dd2e2e2c87845e244df41b72633372b4b9795242f069b3ab2ccbc728756ce8`  
		Last Modified: Thu, 11 Jan 2024 00:04:32 GMT  
		Size: 183.1 MB (183053648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c2cf5808cd6dced23f08a2d0921f88eae3754821b91d2df3decb5d5c8638a6`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:windowsservercore` - windows version 10.0.17763.5329; amd64

```console
$ docker pull julia@sha256:465739c99dd446c2698ee1f7151fc4f82c353749d9bc6b828a0e5e1db645c233
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2252827649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e690842a775a28bffae7fca39b8fa765ab792fabd7d6883bbc561866e2726e`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:03:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:03:43 GMT
ENV JULIA_VERSION=1.10.0
# Thu, 11 Jan 2024 00:03:44 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.0-win64.exe
# Thu, 11 Jan 2024 00:03:44 GMT
ENV JULIA_SHA256=f58aaa631748a5b0389586f3a3b7a081a2a6ac219a5a73a501ac61c0d99daebd
# Thu, 11 Jan 2024 00:05:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:05:27 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9e301d4f97511dcb9f3216268f983f8b8a38f59f6f47d7fcfa6c74bd89340c`  
		Last Modified: Thu, 11 Jan 2024 00:05:35 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15e9906d04250bd67cb869011a80e67292f17770b36865f9ce3b3f07765278f`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6305ccc6bbbc63d35ea2541315eff9b40ff82631ddc08cf97bae6597d416e35d`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fead423ba6e49e59afeb0485520bcfc1ca1f5231bc0104438c670c75c56d67a`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de60c693e3b77965993cdcd8ccef1ce49bbfd61e59f5e5f85a7b950645ce499b`  
		Last Modified: Thu, 11 Jan 2024 00:05:58 GMT  
		Size: 183.1 MB (183098483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ab8928320d6137aceb0a714f2cc037f1c072f50385773b2f6f1d39368da3fc`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore-1809`

```console
$ docker pull julia@sha256:999bd26e0d2f8bf19acbc55dbda3f7303d67f591de5cfdfe5a04914cc44d8c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `julia:windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull julia@sha256:465739c99dd446c2698ee1f7151fc4f82c353749d9bc6b828a0e5e1db645c233
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2252827649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e690842a775a28bffae7fca39b8fa765ab792fabd7d6883bbc561866e2726e`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:03:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:03:43 GMT
ENV JULIA_VERSION=1.10.0
# Thu, 11 Jan 2024 00:03:44 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.0-win64.exe
# Thu, 11 Jan 2024 00:03:44 GMT
ENV JULIA_SHA256=f58aaa631748a5b0389586f3a3b7a081a2a6ac219a5a73a501ac61c0d99daebd
# Thu, 11 Jan 2024 00:05:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:05:27 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9e301d4f97511dcb9f3216268f983f8b8a38f59f6f47d7fcfa6c74bd89340c`  
		Last Modified: Thu, 11 Jan 2024 00:05:35 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15e9906d04250bd67cb869011a80e67292f17770b36865f9ce3b3f07765278f`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6305ccc6bbbc63d35ea2541315eff9b40ff82631ddc08cf97bae6597d416e35d`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fead423ba6e49e59afeb0485520bcfc1ca1f5231bc0104438c670c75c56d67a`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de60c693e3b77965993cdcd8ccef1ce49bbfd61e59f5e5f85a7b950645ce499b`  
		Last Modified: Thu, 11 Jan 2024 00:05:58 GMT  
		Size: 183.1 MB (183098483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ab8928320d6137aceb0a714f2cc037f1c072f50385773b2f6f1d39368da3fc`  
		Last Modified: Thu, 11 Jan 2024 00:05:33 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:473983fe5fe55383db5d0d11749bebef8288fe2bc9eb5a72ab3f76b3e6c45d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `julia:windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull julia@sha256:795c32c108c365c2480a69a195c9a7e377678d314eefe72f64c230c9178355af
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2083272778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe626ae4264c3793e3f2752abc204a549a77a114b9658003d2cda440332150c6`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Thu, 11 Jan 2024 00:02:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:02:52 GMT
ENV JULIA_VERSION=1.10.0
# Thu, 11 Jan 2024 00:02:53 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.0-win64.exe
# Thu, 11 Jan 2024 00:02:54 GMT
ENV JULIA_SHA256=f58aaa631748a5b0389586f3a3b7a081a2a6ac219a5a73a501ac61c0d99daebd
# Thu, 11 Jan 2024 00:04:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:04:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c4a7e196fc6ca93a61a3bbf497fb2b0eca327aa5cf473b95639f61b03c7c1d7`  
		Last Modified: Thu, 11 Jan 2024 00:04:09 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9346ba0550e4beb52f6dad09e1fa6fcd503e75c3df053e5648a54d6dfa7f05`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d7e35a894e972ab63511466519f9a4136a6144e7dbbd6e622be148046ddbaf`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e808d436d368c0aa304f09221c040769d471ae77d9fc07a9bad5a4eff093923`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86dd2e2e2c87845e244df41b72633372b4b9795242f069b3ab2ccbc728756ce8`  
		Last Modified: Thu, 11 Jan 2024 00:04:32 GMT  
		Size: 183.1 MB (183053648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c2cf5808cd6dced23f08a2d0921f88eae3754821b91d2df3decb5d5c8638a6`  
		Last Modified: Thu, 11 Jan 2024 00:04:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
