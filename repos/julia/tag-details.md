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
-	[`julia:1.10.1`](#julia1101)
-	[`julia:1.10.1-alpine`](#julia1101-alpine)
-	[`julia:1.10.1-alpine3.18`](#julia1101-alpine318)
-	[`julia:1.10.1-alpine3.19`](#julia1101-alpine319)
-	[`julia:1.10.1-bookworm`](#julia1101-bookworm)
-	[`julia:1.10.1-bullseye`](#julia1101-bullseye)
-	[`julia:1.10.1-windowsservercore`](#julia1101-windowsservercore)
-	[`julia:1.10.1-windowsservercore-1809`](#julia1101-windowsservercore-1809)
-	[`julia:1.10.1-windowsservercore-ltsc2022`](#julia1101-windowsservercore-ltsc2022)
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
$ docker pull julia@sha256:2d992bcdfd817a11bfa70918879674b62dcd0a497e079116605c33dc9979589e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

### `julia:1` - linux; amd64

```console
$ docker pull julia@sha256:3caf5e0e4797801b5afa0cdb559075e1f7226c7ea16a3153fe7d18769aba94e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.2 MB (205223283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae4a5eea63105374a0e3ad6f704dedf7bf406350ddb98b6ad13582428fa24df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.1-linux-x86_64.tar.gz'; 			sha256='fe924258e55d074410b134195cf6b85cbe8f307fcd05a4fdd23f8944c5941a70'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.1-linux-aarch64.tar.gz'; 			sha256='67e912a2b8ae0fd2469a1a42c7d70b18cdf30b06dc717653fac64b710ca0575e'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.1-linux-i686.tar.gz'; 			sha256='46ae06f5690b4812e091f8e2a1b8a1caf849b5c842e8c7c3b8e474aaa7302526'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b760910a8ea7efbbc01dd05c522c09fbb768992e3e65929cf016f8a28e719d7`  
		Last Modified: Thu, 15 Feb 2024 01:52:52 GMT  
		Size: 5.7 MB (5707930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd429a837e23f6998e27565211ae302823134f3abdcf89d5a7c9400204139c55`  
		Last Modified: Thu, 15 Feb 2024 01:52:56 GMT  
		Size: 170.4 MB (170390890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6284bd0c80ca3e758d54e5f4f5076c25ccebccbba5d1108ef3ba6bc1703e73`  
		Last Modified: Thu, 15 Feb 2024 01:52:52 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:758cf0885b58460ec61796007b01d32c41f514dc0e1f8447e9a99f881f6666dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2158113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13bb7fc6510c67ceb8c7e7b0e22270d2ab6c904c71fc91de34003938191ebee1`

```dockerfile
```

-	Layers:
	-	`sha256:fe238e30162271ec796cf27837b3f1d078051f6979b4a0231cba428ae6598966`  
		Last Modified: Thu, 15 Feb 2024 01:52:52 GMT  
		Size: 2.1 MB (2139403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59fbd28bbcc24b3f7bb1c4f252a545a1236ff7692d9643ab5983bf53d2ef990b`  
		Last Modified: Thu, 15 Feb 2024 01:52:51 GMT  
		Size: 18.7 KB (18710 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:c7899893acb41c45312f7bcdc32512504b58ede63f02a0bba4dca92a272dbfda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.7 MB (199690181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:953f39f3ca0da48a4a5caebe30cc5d44769e6b518af75d4b51ce1f2b85fd7eaa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
CMD ["bash"]
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.1-linux-x86_64.tar.gz'; 			sha256='fe924258e55d074410b134195cf6b85cbe8f307fcd05a4fdd23f8944c5941a70'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.1-linux-aarch64.tar.gz'; 			sha256='67e912a2b8ae0fd2469a1a42c7d70b18cdf30b06dc717653fac64b710ca0575e'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.1-linux-i686.tar.gz'; 			sha256='46ae06f5690b4812e091f8e2a1b8a1caf849b5c842e8c7c3b8e474aaa7302526'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
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
	-	`sha256:df0a7047eef5296003128d4756f1f1b85b64c3f77206da6c62d958fc9572f10a`  
		Last Modified: Thu, 15 Feb 2024 02:14:07 GMT  
		Size: 165.0 MB (165000301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9f16d4c44b43675a53f7695a26f28e3cc7b16e7e71b0dddd82233834973fb3`  
		Last Modified: Thu, 15 Feb 2024 02:14:03 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:aaee047bc50ce902be26894ad0f4f267dda17086bf85430a1159a7ca679533de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2157334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c644ea6ef587504b4b31a9b2946c85895ec0a36586b46679c63753215cc4b8cd`

```dockerfile
```

-	Layers:
	-	`sha256:6ef921af30be56f765d798735060cdf175b864621010058e5c33ad36ac7a00b9`  
		Last Modified: Thu, 15 Feb 2024 02:14:03 GMT  
		Size: 2.1 MB (2138773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6bbf6d09ba5d03bb45cd1ca38605efef1b6f6227352ec90c0d7041a312e1e03`  
		Last Modified: Thu, 15 Feb 2024 02:14:03 GMT  
		Size: 18.6 KB (18561 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - linux; 386

```console
$ docker pull julia@sha256:c733805bb2115e3e7ac2293646a60c5c37145d14575ae13a887543f7cfcfb120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192500887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27155dea2c1a627acfc854ba5afb07edabdbf706f1d74a0df905d2af1d98ace`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:56 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Tue, 13 Feb 2024 00:38:56 GMT
CMD ["bash"]
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.1-linux-x86_64.tar.gz'; 			sha256='fe924258e55d074410b134195cf6b85cbe8f307fcd05a4fdd23f8944c5941a70'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.1-linux-aarch64.tar.gz'; 			sha256='67e912a2b8ae0fd2469a1a42c7d70b18cdf30b06dc717653fac64b710ca0575e'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.1-linux-i686.tar.gz'; 			sha256='46ae06f5690b4812e091f8e2a1b8a1caf849b5c842e8c7c3b8e474aaa7302526'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b060bee81687c0dd068e9e9bb305e7d29ed2e3599f2ad66b28f8b70956a9fd21`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 5.9 MB (5863219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0a9393e3d7ec1e1d267186dd2e07326e97b56b875a4bb284b88b54504d9121`  
		Last Modified: Thu, 15 Feb 2024 01:52:46 GMT  
		Size: 156.5 MB (156495490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28dd21637325ca9b78d6c7e0a451b94a842713f5d96b2dfe69077bd35f7b44f`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:1460d63336cc97e4810367a540f40251647c57e6c86390c26469cf7da2b54930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2155240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4e048bdbabc6b4032e5cab36750926cf4d48be404b13f1d86268c55af218916`

```dockerfile
```

-	Layers:
	-	`sha256:0c29468e89b817688be1fa9de743c5e24910501b2881091894d40e5e6a71c2cb`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 2.1 MB (2136581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdd8305c04fcac3daa8caffcbcc79c942a6871f59a617792ec7e5741cc95c75b`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 18.7 KB (18659 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - windows version 10.0.20348.2322; amd64

```console
$ docker pull julia@sha256:ac7e7de1919e6a391278fd06062034d24dd1892f6569260439ea7a8aac745dd0
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2161166383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f26f77914b415046af8c139841e565707106b2048fc516c6c1cb8347d2a4f8`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Thu, 15 Feb 2024 01:55:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 15 Feb 2024 01:55:58 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 01:55:58 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.1-win64.exe
# Thu, 15 Feb 2024 01:55:59 GMT
ENV JULIA_SHA256=ca02e6bd4f771d51c72520f359d727679775c03f62e7e7e2595dd79d1d0e5fec
# Thu, 15 Feb 2024 01:57:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 15 Feb 2024 01:57:04 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ecd8f02f1b59d6f3aec1c570f2c8128d2b064a59e0da86653fdee442a472ad`  
		Last Modified: Thu, 15 Feb 2024 01:57:11 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62852f81701e842eaa34fb5baf41629e3a8bd717a09aeae6c9d8f85aa6d3d870`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a1387c2ad061bd6ecc5941ab04b037b84018b2bfddaa265150d148ffca73b4`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f3360ff5dce5375b4b898a4f4deb9f588e12659cb8db5611d7e3e01952b012`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44ebaee761d2302e12dcc0f6dc0d9e5debeb07658857a8749c1f96a07fa3bfb`  
		Last Modified: Thu, 15 Feb 2024 01:58:16 GMT  
		Size: 250.5 MB (250505768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c23a6fdc0fc3d51f4f3676cdf3a438f7d52cb9f9a6a964c4645f304cf900ff`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1` - windows version 10.0.17763.5458; amd64

```console
$ docker pull julia@sha256:0955c5756b87875173c9a5b65b2df8cbb7d5b390c9c4550f7f521c40b3fa1935
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2330962381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef0a0692cd89c0ebd705bcc2f6c2ddf0fa8c2f800111fbf1041ec324ce62832a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Thu, 15 Feb 2024 02:05:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 15 Feb 2024 02:05:41 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 02:05:42 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.1-win64.exe
# Thu, 15 Feb 2024 02:05:43 GMT
ENV JULIA_SHA256=ca02e6bd4f771d51c72520f359d727679775c03f62e7e7e2595dd79d1d0e5fec
# Thu, 15 Feb 2024 02:07:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 15 Feb 2024 02:07:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ed3e36144d60ff8117a3dd6eb64daa4e29953bb129aaad397b30092f9cc4c1`  
		Last Modified: Thu, 15 Feb 2024 02:07:25 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ff9d169a5e63801023c2b6a0a537977e5c7505d96e3c8896d7dfeadf1d0072`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948476976b5affd175205c3463e19547505c660c8d62ec0c51a0ccab24e7a100`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3066dd587e2e5fd44cc77bcf785a1eda6cb2c8fbfea705e112683712dc9bbf45`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de535d017baa9a7dbbcba70d7fde8cdb8607907fd1752fa99946ddf57958b2b0`  
		Last Modified: Thu, 15 Feb 2024 02:08:00 GMT  
		Size: 250.5 MB (250507125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1858c84143178e070fff903c762901603d1b1356e962f4fb73a71a200a55c84c`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-alpine`

```console
$ docker pull julia@sha256:38e9661d58c48669b03a2b9be0bb4c4fb995f270442388854bab380043c41e2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1-alpine` - linux; amd64

```console
$ docker pull julia@sha256:da0ebe0fdd8d2973c4cbe6c0b441739707a9173f47bf641dc5a0ded3e2d8ad4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.6 MB (177599522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4629a432942eac3a84338692a5217c4758a13da1e447a17b943a4ee5d0cf6357`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.1-musl-x86_64.tar.gz'; 			sha256='48e643c431f156e0cec440e3881f09dd78491c59de7804c73f470fba8cd64d1d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68eaf8cd85ce8bc2f83dd044858e77dc6ea04d797dcee4d4619f3a1dde5f73f1`  
		Last Modified: Thu, 15 Feb 2024 01:52:38 GMT  
		Size: 174.2 MB (174190425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e61b9b3f6995be6208e105dc44d9228d5bc22dc0570c34dbc7dfdd0dfb21b9e`  
		Last Modified: Thu, 15 Feb 2024 01:52:36 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-alpine` - unknown; unknown

```console
$ docker pull julia@sha256:07ab0484248a0b54bc9ccb67a15926fee6ecc1962552ddb0fc93651894af2a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.5 KB (119496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd5b516084ce3e9b080769c76191451657aab08f6d5bebe3ef5668280c39380`

```dockerfile
```

-	Layers:
	-	`sha256:ecaca48c94c6b70ef43edb0d3450d5d2d4cf2a5f5f18ef3b14326697c0a7c529`  
		Last Modified: Thu, 15 Feb 2024 01:52:36 GMT  
		Size: 104.8 KB (104799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bba9bd77ce2c5fd4ab756f06d5010801f772e290016bf8c6a1fc066d5c37d42`  
		Last Modified: Thu, 15 Feb 2024 01:52:36 GMT  
		Size: 14.7 KB (14697 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1-alpine3.18`

```console
$ docker pull julia@sha256:4ec8fa66b1b062c5c7d0ce6c0796ba0c4ea4e5df6cfc03e43e30167e3eb30ad2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1-alpine3.18` - linux; amd64

```console
$ docker pull julia@sha256:e2e9526bf3bab718c84a9929115093953198eb43106374f04f9820f47c25997e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.6 MB (177593364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba54d9793c9d669939bcee642131032584105a0feaad52c06e388cf0d9e219b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.1-musl-x86_64.tar.gz'; 			sha256='48e643c431f156e0cec440e3881f09dd78491c59de7804c73f470fba8cd64d1d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=alpine&os_version=3.18"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef7909ee5233603cda10c2ca32601363045f0197c5f7ce5a3ab10251331176b`  
		Last Modified: Thu, 15 Feb 2024 01:52:50 GMT  
		Size: 174.2 MB (174190453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815110e9a9cb295a7eda0be2b78d3ce7016aa3a82d3d1b7791caf3bc003d9324`  
		Last Modified: Thu, 15 Feb 2024 01:52:47 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-alpine3.18` - unknown; unknown

```console
$ docker pull julia@sha256:7ae9f8f1ea5c2931c587ba63d2a8767bd35581eaf529e7390360469a88ec3434
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.5 KB (116519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df13cc1780fc7df1654365138f14d5147b21018d3a1d5f7238a0ac203b04b87e`

```dockerfile
```

-	Layers:
	-	`sha256:6fd0845ed3571a63743ec9da097c8e95cd1eb993e6cc66e605d7aaf438f3675a`  
		Last Modified: Thu, 15 Feb 2024 01:52:47 GMT  
		Size: 103.0 KB (103033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1393768754e0e0cd1f9f537f6a992341f9030f04e0e05217179713c8e4a0e4f`  
		Last Modified: Thu, 15 Feb 2024 01:52:47 GMT  
		Size: 13.5 KB (13486 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1-alpine3.19`

```console
$ docker pull julia@sha256:38e9661d58c48669b03a2b9be0bb4c4fb995f270442388854bab380043c41e2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1-alpine3.19` - linux; amd64

```console
$ docker pull julia@sha256:da0ebe0fdd8d2973c4cbe6c0b441739707a9173f47bf641dc5a0ded3e2d8ad4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.6 MB (177599522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4629a432942eac3a84338692a5217c4758a13da1e447a17b943a4ee5d0cf6357`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.1-musl-x86_64.tar.gz'; 			sha256='48e643c431f156e0cec440e3881f09dd78491c59de7804c73f470fba8cd64d1d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68eaf8cd85ce8bc2f83dd044858e77dc6ea04d797dcee4d4619f3a1dde5f73f1`  
		Last Modified: Thu, 15 Feb 2024 01:52:38 GMT  
		Size: 174.2 MB (174190425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e61b9b3f6995be6208e105dc44d9228d5bc22dc0570c34dbc7dfdd0dfb21b9e`  
		Last Modified: Thu, 15 Feb 2024 01:52:36 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-alpine3.19` - unknown; unknown

```console
$ docker pull julia@sha256:07ab0484248a0b54bc9ccb67a15926fee6ecc1962552ddb0fc93651894af2a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.5 KB (119496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd5b516084ce3e9b080769c76191451657aab08f6d5bebe3ef5668280c39380`

```dockerfile
```

-	Layers:
	-	`sha256:ecaca48c94c6b70ef43edb0d3450d5d2d4cf2a5f5f18ef3b14326697c0a7c529`  
		Last Modified: Thu, 15 Feb 2024 01:52:36 GMT  
		Size: 104.8 KB (104799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bba9bd77ce2c5fd4ab756f06d5010801f772e290016bf8c6a1fc066d5c37d42`  
		Last Modified: Thu, 15 Feb 2024 01:52:36 GMT  
		Size: 14.7 KB (14697 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1-bookworm`

```console
$ docker pull julia@sha256:687d51426b84545c07df8d8e90a6d40c8a9ecc6a4d1ec6143d3d8237a9d5d0dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:3caf5e0e4797801b5afa0cdb559075e1f7226c7ea16a3153fe7d18769aba94e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.2 MB (205223283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae4a5eea63105374a0e3ad6f704dedf7bf406350ddb98b6ad13582428fa24df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.1-linux-x86_64.tar.gz'; 			sha256='fe924258e55d074410b134195cf6b85cbe8f307fcd05a4fdd23f8944c5941a70'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.1-linux-aarch64.tar.gz'; 			sha256='67e912a2b8ae0fd2469a1a42c7d70b18cdf30b06dc717653fac64b710ca0575e'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.1-linux-i686.tar.gz'; 			sha256='46ae06f5690b4812e091f8e2a1b8a1caf849b5c842e8c7c3b8e474aaa7302526'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b760910a8ea7efbbc01dd05c522c09fbb768992e3e65929cf016f8a28e719d7`  
		Last Modified: Thu, 15 Feb 2024 01:52:52 GMT  
		Size: 5.7 MB (5707930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd429a837e23f6998e27565211ae302823134f3abdcf89d5a7c9400204139c55`  
		Last Modified: Thu, 15 Feb 2024 01:52:56 GMT  
		Size: 170.4 MB (170390890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6284bd0c80ca3e758d54e5f4f5076c25ccebccbba5d1108ef3ba6bc1703e73`  
		Last Modified: Thu, 15 Feb 2024 01:52:52 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:758cf0885b58460ec61796007b01d32c41f514dc0e1f8447e9a99f881f6666dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2158113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13bb7fc6510c67ceb8c7e7b0e22270d2ab6c904c71fc91de34003938191ebee1`

```dockerfile
```

-	Layers:
	-	`sha256:fe238e30162271ec796cf27837b3f1d078051f6979b4a0231cba428ae6598966`  
		Last Modified: Thu, 15 Feb 2024 01:52:52 GMT  
		Size: 2.1 MB (2139403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59fbd28bbcc24b3f7bb1c4f252a545a1236ff7692d9643ab5983bf53d2ef990b`  
		Last Modified: Thu, 15 Feb 2024 01:52:51 GMT  
		Size: 18.7 KB (18710 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:c7899893acb41c45312f7bcdc32512504b58ede63f02a0bba4dca92a272dbfda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.7 MB (199690181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:953f39f3ca0da48a4a5caebe30cc5d44769e6b518af75d4b51ce1f2b85fd7eaa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
CMD ["bash"]
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.1-linux-x86_64.tar.gz'; 			sha256='fe924258e55d074410b134195cf6b85cbe8f307fcd05a4fdd23f8944c5941a70'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.1-linux-aarch64.tar.gz'; 			sha256='67e912a2b8ae0fd2469a1a42c7d70b18cdf30b06dc717653fac64b710ca0575e'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.1-linux-i686.tar.gz'; 			sha256='46ae06f5690b4812e091f8e2a1b8a1caf849b5c842e8c7c3b8e474aaa7302526'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
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
	-	`sha256:df0a7047eef5296003128d4756f1f1b85b64c3f77206da6c62d958fc9572f10a`  
		Last Modified: Thu, 15 Feb 2024 02:14:07 GMT  
		Size: 165.0 MB (165000301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9f16d4c44b43675a53f7695a26f28e3cc7b16e7e71b0dddd82233834973fb3`  
		Last Modified: Thu, 15 Feb 2024 02:14:03 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:aaee047bc50ce902be26894ad0f4f267dda17086bf85430a1159a7ca679533de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2157334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c644ea6ef587504b4b31a9b2946c85895ec0a36586b46679c63753215cc4b8cd`

```dockerfile
```

-	Layers:
	-	`sha256:6ef921af30be56f765d798735060cdf175b864621010058e5c33ad36ac7a00b9`  
		Last Modified: Thu, 15 Feb 2024 02:14:03 GMT  
		Size: 2.1 MB (2138773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6bbf6d09ba5d03bb45cd1ca38605efef1b6f6227352ec90c0d7041a312e1e03`  
		Last Modified: Thu, 15 Feb 2024 02:14:03 GMT  
		Size: 18.6 KB (18561 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; 386

```console
$ docker pull julia@sha256:c733805bb2115e3e7ac2293646a60c5c37145d14575ae13a887543f7cfcfb120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192500887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27155dea2c1a627acfc854ba5afb07edabdbf706f1d74a0df905d2af1d98ace`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:56 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Tue, 13 Feb 2024 00:38:56 GMT
CMD ["bash"]
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.1-linux-x86_64.tar.gz'; 			sha256='fe924258e55d074410b134195cf6b85cbe8f307fcd05a4fdd23f8944c5941a70'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.1-linux-aarch64.tar.gz'; 			sha256='67e912a2b8ae0fd2469a1a42c7d70b18cdf30b06dc717653fac64b710ca0575e'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.1-linux-i686.tar.gz'; 			sha256='46ae06f5690b4812e091f8e2a1b8a1caf849b5c842e8c7c3b8e474aaa7302526'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b060bee81687c0dd068e9e9bb305e7d29ed2e3599f2ad66b28f8b70956a9fd21`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 5.9 MB (5863219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0a9393e3d7ec1e1d267186dd2e07326e97b56b875a4bb284b88b54504d9121`  
		Last Modified: Thu, 15 Feb 2024 01:52:46 GMT  
		Size: 156.5 MB (156495490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28dd21637325ca9b78d6c7e0a451b94a842713f5d96b2dfe69077bd35f7b44f`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:1460d63336cc97e4810367a540f40251647c57e6c86390c26469cf7da2b54930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2155240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4e048bdbabc6b4032e5cab36750926cf4d48be404b13f1d86268c55af218916`

```dockerfile
```

-	Layers:
	-	`sha256:0c29468e89b817688be1fa9de743c5e24910501b2881091894d40e5e6a71c2cb`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 2.1 MB (2136581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdd8305c04fcac3daa8caffcbcc79c942a6871f59a617792ec7e5741cc95c75b`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 18.7 KB (18659 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1-bullseye`

```console
$ docker pull julia@sha256:7ad8dfad6efa322a660d6dd97a4f51d593e5ca3af248a8a10b07536169c13d28
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
$ docker pull julia@sha256:24c742c0cc59e688cca2b4064189e37ed35878c7f1709a2cffa3c8d89d64ddc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.2 MB (204239761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a882b29e497eb3cbd9ee464ae98d65cf2af1741338cc88dd8761fada5fb008`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.1-linux-x86_64.tar.gz'; 			sha256='fe924258e55d074410b134195cf6b85cbe8f307fcd05a4fdd23f8944c5941a70'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.1-linux-aarch64.tar.gz'; 			sha256='67e912a2b8ae0fd2469a1a42c7d70b18cdf30b06dc717653fac64b710ca0575e'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.1-linux-i686.tar.gz'; 			sha256='46ae06f5690b4812e091f8e2a1b8a1caf849b5c842e8c7c3b8e474aaa7302526'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52994ac9c626986c541c9af48e43ce1e0640e1923e36e90f5d0fac837147ce4f`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 2.4 MB (2426548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2953fea1f932882e3271c8cb61836952f6f90cfbaa344e8986500308c0cfe350`  
		Last Modified: Thu, 15 Feb 2024 01:52:45 GMT  
		Size: 170.4 MB (170390420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ddfead841b8c9404e76dd94b0b7a2340f8535ae2519d8fadfd50f6910a3b50a`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:2d799f94368b3ce51d7c73df4f866409c4274bbdd86f24af6604befc903ff1a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f294f1fdee6ae56922f01b720082730221f68e19fb7128cd6b956ec44ef36124`

```dockerfile
```

-	Layers:
	-	`sha256:74f859ebca0253d35bc9e06a1902608fa6958f913875dd6c9c4332601900ef57`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 2.4 MB (2359909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b86568a9b88e5470630bc40bf42cf53d203c35ff5d496a57d2f38fc9565de2c`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 17.5 KB (17540 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:99a7a3642824f780c5063e3332f761b4254397660f29b86033ee0c76042d8c42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.5 MB (197487223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e371987ac33efcf3b92b1e37091a25ce5adf8792a55f6670ffdf9ae1217acb3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.1-linux-x86_64.tar.gz'; 			sha256='fe924258e55d074410b134195cf6b85cbe8f307fcd05a4fdd23f8944c5941a70'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.1-linux-aarch64.tar.gz'; 			sha256='67e912a2b8ae0fd2469a1a42c7d70b18cdf30b06dc717653fac64b710ca0575e'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.1-linux-i686.tar.gz'; 			sha256='46ae06f5690b4812e091f8e2a1b8a1caf849b5c842e8c7c3b8e474aaa7302526'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
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
	-	`sha256:4fdc35222d7fcab46d11964d7e268775a9e4dbeebda85291a301ed8e3f38f12d`  
		Last Modified: Thu, 15 Feb 2024 02:15:10 GMT  
		Size: 165.0 MB (165000735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad69da563be9c7b3dc8b611885665f62220ebe6398e81be8b290f77b0269b90`  
		Last Modified: Thu, 15 Feb 2024 02:15:07 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:b8ff89e6d9cbd111de03fc482476ae6906c3e816120f66197e3238d29dd1f98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2376644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0a75eebe54c1ec99e9c01002195b63a859a0886f69df77d25e26c0ea55014bd`

```dockerfile
```

-	Layers:
	-	`sha256:8dc77e10839b1fb9c0dec75843295adca36d084e87b48ada981a892c3778d312`  
		Last Modified: Thu, 15 Feb 2024 02:15:06 GMT  
		Size: 2.4 MB (2359261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18b6801e86d58f2bb78f3906b735cd5539178e9c21fcfaeea7db87c57d3d825b`  
		Last Modified: Thu, 15 Feb 2024 02:15:06 GMT  
		Size: 17.4 KB (17383 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bullseye` - linux; 386

```console
$ docker pull julia@sha256:4cc3e8cc1fc2445d3c8958223fb7ff3ed7386fcc59053b4fbb52caa0b8b135f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191436740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a89c723882a8e89f126a53b96a86330d39b04f7fd394adb5be01967629f4a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:18 GMT
ADD file:9eaee5af136d095dc1dac0ffce0fde09d8f1bd02ff7cb65ee67e00b2a66f34f7 in / 
# Tue, 13 Feb 2024 00:39:19 GMT
CMD ["bash"]
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.1-linux-x86_64.tar.gz'; 			sha256='fe924258e55d074410b134195cf6b85cbe8f307fcd05a4fdd23f8944c5941a70'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.1-linux-aarch64.tar.gz'; 			sha256='67e912a2b8ae0fd2469a1a42c7d70b18cdf30b06dc717653fac64b710ca0575e'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.1-linux-i686.tar.gz'; 			sha256='46ae06f5690b4812e091f8e2a1b8a1caf849b5c842e8c7c3b8e474aaa7302526'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1ac8173b08d16f9f136fb0e3ee39999cef7495f924ecb43f3ca4a4eea267cc88`  
		Last Modified: Tue, 13 Feb 2024 00:44:36 GMT  
		Size: 32.4 MB (32407443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c2a21aba0b258d2d59ed768ff41751fcc88255368a239a0c26c72579e241ac`  
		Last Modified: Thu, 15 Feb 2024 01:52:40 GMT  
		Size: 2.5 MB (2533021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d246a08907e76876dc75135451dddc888bc48ceee300a8336e3172f79d0d246`  
		Last Modified: Thu, 15 Feb 2024 01:52:44 GMT  
		Size: 156.5 MB (156495904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45acd41394aa2be9e84237ed4d84fb4b41efa03ffdae3fee7ffe23d93fcc587f`  
		Last Modified: Thu, 15 Feb 2024 01:52:40 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:f324c95527f73df472f020fe9ad52ca74da2c87ea065cfc19eecf21d5d5ee350
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2374624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da94324fe8ee54c3188af2712264ee35eb43fcfbd1ffcfaff78c507270b0b33`

```dockerfile
```

-	Layers:
	-	`sha256:cbf974f51c72a3dabef9dfde0558dc77052a511c4f7b23f57744ad1d82a71698`  
		Last Modified: Thu, 15 Feb 2024 01:52:40 GMT  
		Size: 2.4 MB (2357115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44c5e6153327499afffa4e26339c505637b4ed975cb6175112ad50d21df77e8d`  
		Last Modified: Thu, 15 Feb 2024 01:52:40 GMT  
		Size: 17.5 KB (17509 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1-windowsservercore`

```console
$ docker pull julia@sha256:91949f9dc6a2ba335f38712cd941eb739d1c64a260fde1059319857eab40e0e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

### `julia:1-windowsservercore` - windows version 10.0.20348.2322; amd64

```console
$ docker pull julia@sha256:ac7e7de1919e6a391278fd06062034d24dd1892f6569260439ea7a8aac745dd0
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2161166383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f26f77914b415046af8c139841e565707106b2048fc516c6c1cb8347d2a4f8`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Thu, 15 Feb 2024 01:55:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 15 Feb 2024 01:55:58 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 01:55:58 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.1-win64.exe
# Thu, 15 Feb 2024 01:55:59 GMT
ENV JULIA_SHA256=ca02e6bd4f771d51c72520f359d727679775c03f62e7e7e2595dd79d1d0e5fec
# Thu, 15 Feb 2024 01:57:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 15 Feb 2024 01:57:04 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ecd8f02f1b59d6f3aec1c570f2c8128d2b064a59e0da86653fdee442a472ad`  
		Last Modified: Thu, 15 Feb 2024 01:57:11 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62852f81701e842eaa34fb5baf41629e3a8bd717a09aeae6c9d8f85aa6d3d870`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a1387c2ad061bd6ecc5941ab04b037b84018b2bfddaa265150d148ffca73b4`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f3360ff5dce5375b4b898a4f4deb9f588e12659cb8db5611d7e3e01952b012`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44ebaee761d2302e12dcc0f6dc0d9e5debeb07658857a8749c1f96a07fa3bfb`  
		Last Modified: Thu, 15 Feb 2024 01:58:16 GMT  
		Size: 250.5 MB (250505768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c23a6fdc0fc3d51f4f3676cdf3a438f7d52cb9f9a6a964c4645f304cf900ff`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-windowsservercore` - windows version 10.0.17763.5458; amd64

```console
$ docker pull julia@sha256:0955c5756b87875173c9a5b65b2df8cbb7d5b390c9c4550f7f521c40b3fa1935
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2330962381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef0a0692cd89c0ebd705bcc2f6c2ddf0fa8c2f800111fbf1041ec324ce62832a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Thu, 15 Feb 2024 02:05:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 15 Feb 2024 02:05:41 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 02:05:42 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.1-win64.exe
# Thu, 15 Feb 2024 02:05:43 GMT
ENV JULIA_SHA256=ca02e6bd4f771d51c72520f359d727679775c03f62e7e7e2595dd79d1d0e5fec
# Thu, 15 Feb 2024 02:07:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 15 Feb 2024 02:07:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ed3e36144d60ff8117a3dd6eb64daa4e29953bb129aaad397b30092f9cc4c1`  
		Last Modified: Thu, 15 Feb 2024 02:07:25 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ff9d169a5e63801023c2b6a0a537977e5c7505d96e3c8896d7dfeadf1d0072`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948476976b5affd175205c3463e19547505c660c8d62ec0c51a0ccab24e7a100`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3066dd587e2e5fd44cc77bcf785a1eda6cb2c8fbfea705e112683712dc9bbf45`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de535d017baa9a7dbbcba70d7fde8cdb8607907fd1752fa99946ddf57958b2b0`  
		Last Modified: Thu, 15 Feb 2024 02:08:00 GMT  
		Size: 250.5 MB (250507125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1858c84143178e070fff903c762901603d1b1356e962f4fb73a71a200a55c84c`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore-1809`

```console
$ docker pull julia@sha256:8720bbebce56e70f307b6ac3cd3d43e9f56b62fb168aade64cdb8abadc92f745
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `julia:1-windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull julia@sha256:0955c5756b87875173c9a5b65b2df8cbb7d5b390c9c4550f7f521c40b3fa1935
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2330962381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef0a0692cd89c0ebd705bcc2f6c2ddf0fa8c2f800111fbf1041ec324ce62832a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Thu, 15 Feb 2024 02:05:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 15 Feb 2024 02:05:41 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 02:05:42 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.1-win64.exe
# Thu, 15 Feb 2024 02:05:43 GMT
ENV JULIA_SHA256=ca02e6bd4f771d51c72520f359d727679775c03f62e7e7e2595dd79d1d0e5fec
# Thu, 15 Feb 2024 02:07:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 15 Feb 2024 02:07:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ed3e36144d60ff8117a3dd6eb64daa4e29953bb129aaad397b30092f9cc4c1`  
		Last Modified: Thu, 15 Feb 2024 02:07:25 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ff9d169a5e63801023c2b6a0a537977e5c7505d96e3c8896d7dfeadf1d0072`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948476976b5affd175205c3463e19547505c660c8d62ec0c51a0ccab24e7a100`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3066dd587e2e5fd44cc77bcf785a1eda6cb2c8fbfea705e112683712dc9bbf45`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de535d017baa9a7dbbcba70d7fde8cdb8607907fd1752fa99946ddf57958b2b0`  
		Last Modified: Thu, 15 Feb 2024 02:08:00 GMT  
		Size: 250.5 MB (250507125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1858c84143178e070fff903c762901603d1b1356e962f4fb73a71a200a55c84c`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:9a0e4ffc6087aabba7828052356da4cfbfb1db8f47eba6afec0c6bf93a96f3a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2322; amd64

### `julia:1-windowsservercore-ltsc2022` - windows version 10.0.20348.2322; amd64

```console
$ docker pull julia@sha256:ac7e7de1919e6a391278fd06062034d24dd1892f6569260439ea7a8aac745dd0
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2161166383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f26f77914b415046af8c139841e565707106b2048fc516c6c1cb8347d2a4f8`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Thu, 15 Feb 2024 01:55:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 15 Feb 2024 01:55:58 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 01:55:58 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.1-win64.exe
# Thu, 15 Feb 2024 01:55:59 GMT
ENV JULIA_SHA256=ca02e6bd4f771d51c72520f359d727679775c03f62e7e7e2595dd79d1d0e5fec
# Thu, 15 Feb 2024 01:57:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 15 Feb 2024 01:57:04 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ecd8f02f1b59d6f3aec1c570f2c8128d2b064a59e0da86653fdee442a472ad`  
		Last Modified: Thu, 15 Feb 2024 01:57:11 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62852f81701e842eaa34fb5baf41629e3a8bd717a09aeae6c9d8f85aa6d3d870`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a1387c2ad061bd6ecc5941ab04b037b84018b2bfddaa265150d148ffca73b4`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f3360ff5dce5375b4b898a4f4deb9f588e12659cb8db5611d7e3e01952b012`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44ebaee761d2302e12dcc0f6dc0d9e5debeb07658857a8749c1f96a07fa3bfb`  
		Last Modified: Thu, 15 Feb 2024 01:58:16 GMT  
		Size: 250.5 MB (250505768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c23a6fdc0fc3d51f4f3676cdf3a438f7d52cb9f9a6a964c4645f304cf900ff`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10`

```console
$ docker pull julia@sha256:2d992bcdfd817a11bfa70918879674b62dcd0a497e079116605c33dc9979589e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

### `julia:1.10` - linux; amd64

```console
$ docker pull julia@sha256:3caf5e0e4797801b5afa0cdb559075e1f7226c7ea16a3153fe7d18769aba94e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.2 MB (205223283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae4a5eea63105374a0e3ad6f704dedf7bf406350ddb98b6ad13582428fa24df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.1-linux-x86_64.tar.gz'; 			sha256='fe924258e55d074410b134195cf6b85cbe8f307fcd05a4fdd23f8944c5941a70'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.1-linux-aarch64.tar.gz'; 			sha256='67e912a2b8ae0fd2469a1a42c7d70b18cdf30b06dc717653fac64b710ca0575e'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.1-linux-i686.tar.gz'; 			sha256='46ae06f5690b4812e091f8e2a1b8a1caf849b5c842e8c7c3b8e474aaa7302526'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b760910a8ea7efbbc01dd05c522c09fbb768992e3e65929cf016f8a28e719d7`  
		Last Modified: Thu, 15 Feb 2024 01:52:52 GMT  
		Size: 5.7 MB (5707930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd429a837e23f6998e27565211ae302823134f3abdcf89d5a7c9400204139c55`  
		Last Modified: Thu, 15 Feb 2024 01:52:56 GMT  
		Size: 170.4 MB (170390890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6284bd0c80ca3e758d54e5f4f5076c25ccebccbba5d1108ef3ba6bc1703e73`  
		Last Modified: Thu, 15 Feb 2024 01:52:52 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:758cf0885b58460ec61796007b01d32c41f514dc0e1f8447e9a99f881f6666dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2158113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13bb7fc6510c67ceb8c7e7b0e22270d2ab6c904c71fc91de34003938191ebee1`

```dockerfile
```

-	Layers:
	-	`sha256:fe238e30162271ec796cf27837b3f1d078051f6979b4a0231cba428ae6598966`  
		Last Modified: Thu, 15 Feb 2024 01:52:52 GMT  
		Size: 2.1 MB (2139403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59fbd28bbcc24b3f7bb1c4f252a545a1236ff7692d9643ab5983bf53d2ef990b`  
		Last Modified: Thu, 15 Feb 2024 01:52:51 GMT  
		Size: 18.7 KB (18710 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:c7899893acb41c45312f7bcdc32512504b58ede63f02a0bba4dca92a272dbfda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.7 MB (199690181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:953f39f3ca0da48a4a5caebe30cc5d44769e6b518af75d4b51ce1f2b85fd7eaa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
CMD ["bash"]
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.1-linux-x86_64.tar.gz'; 			sha256='fe924258e55d074410b134195cf6b85cbe8f307fcd05a4fdd23f8944c5941a70'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.1-linux-aarch64.tar.gz'; 			sha256='67e912a2b8ae0fd2469a1a42c7d70b18cdf30b06dc717653fac64b710ca0575e'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.1-linux-i686.tar.gz'; 			sha256='46ae06f5690b4812e091f8e2a1b8a1caf849b5c842e8c7c3b8e474aaa7302526'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
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
	-	`sha256:df0a7047eef5296003128d4756f1f1b85b64c3f77206da6c62d958fc9572f10a`  
		Last Modified: Thu, 15 Feb 2024 02:14:07 GMT  
		Size: 165.0 MB (165000301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9f16d4c44b43675a53f7695a26f28e3cc7b16e7e71b0dddd82233834973fb3`  
		Last Modified: Thu, 15 Feb 2024 02:14:03 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:aaee047bc50ce902be26894ad0f4f267dda17086bf85430a1159a7ca679533de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2157334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c644ea6ef587504b4b31a9b2946c85895ec0a36586b46679c63753215cc4b8cd`

```dockerfile
```

-	Layers:
	-	`sha256:6ef921af30be56f765d798735060cdf175b864621010058e5c33ad36ac7a00b9`  
		Last Modified: Thu, 15 Feb 2024 02:14:03 GMT  
		Size: 2.1 MB (2138773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6bbf6d09ba5d03bb45cd1ca38605efef1b6f6227352ec90c0d7041a312e1e03`  
		Last Modified: Thu, 15 Feb 2024 02:14:03 GMT  
		Size: 18.6 KB (18561 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; 386

```console
$ docker pull julia@sha256:c733805bb2115e3e7ac2293646a60c5c37145d14575ae13a887543f7cfcfb120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192500887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27155dea2c1a627acfc854ba5afb07edabdbf706f1d74a0df905d2af1d98ace`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:56 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Tue, 13 Feb 2024 00:38:56 GMT
CMD ["bash"]
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.1-linux-x86_64.tar.gz'; 			sha256='fe924258e55d074410b134195cf6b85cbe8f307fcd05a4fdd23f8944c5941a70'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.1-linux-aarch64.tar.gz'; 			sha256='67e912a2b8ae0fd2469a1a42c7d70b18cdf30b06dc717653fac64b710ca0575e'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.1-linux-i686.tar.gz'; 			sha256='46ae06f5690b4812e091f8e2a1b8a1caf849b5c842e8c7c3b8e474aaa7302526'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b060bee81687c0dd068e9e9bb305e7d29ed2e3599f2ad66b28f8b70956a9fd21`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 5.9 MB (5863219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0a9393e3d7ec1e1d267186dd2e07326e97b56b875a4bb284b88b54504d9121`  
		Last Modified: Thu, 15 Feb 2024 01:52:46 GMT  
		Size: 156.5 MB (156495490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28dd21637325ca9b78d6c7e0a451b94a842713f5d96b2dfe69077bd35f7b44f`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:1460d63336cc97e4810367a540f40251647c57e6c86390c26469cf7da2b54930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2155240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4e048bdbabc6b4032e5cab36750926cf4d48be404b13f1d86268c55af218916`

```dockerfile
```

-	Layers:
	-	`sha256:0c29468e89b817688be1fa9de743c5e24910501b2881091894d40e5e6a71c2cb`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 2.1 MB (2136581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdd8305c04fcac3daa8caffcbcc79c942a6871f59a617792ec7e5741cc95c75b`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 18.7 KB (18659 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - windows version 10.0.20348.2322; amd64

```console
$ docker pull julia@sha256:ac7e7de1919e6a391278fd06062034d24dd1892f6569260439ea7a8aac745dd0
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2161166383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f26f77914b415046af8c139841e565707106b2048fc516c6c1cb8347d2a4f8`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Thu, 15 Feb 2024 01:55:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 15 Feb 2024 01:55:58 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 01:55:58 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.1-win64.exe
# Thu, 15 Feb 2024 01:55:59 GMT
ENV JULIA_SHA256=ca02e6bd4f771d51c72520f359d727679775c03f62e7e7e2595dd79d1d0e5fec
# Thu, 15 Feb 2024 01:57:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 15 Feb 2024 01:57:04 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ecd8f02f1b59d6f3aec1c570f2c8128d2b064a59e0da86653fdee442a472ad`  
		Last Modified: Thu, 15 Feb 2024 01:57:11 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62852f81701e842eaa34fb5baf41629e3a8bd717a09aeae6c9d8f85aa6d3d870`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a1387c2ad061bd6ecc5941ab04b037b84018b2bfddaa265150d148ffca73b4`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f3360ff5dce5375b4b898a4f4deb9f588e12659cb8db5611d7e3e01952b012`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44ebaee761d2302e12dcc0f6dc0d9e5debeb07658857a8749c1f96a07fa3bfb`  
		Last Modified: Thu, 15 Feb 2024 01:58:16 GMT  
		Size: 250.5 MB (250505768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c23a6fdc0fc3d51f4f3676cdf3a438f7d52cb9f9a6a964c4645f304cf900ff`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10` - windows version 10.0.17763.5458; amd64

```console
$ docker pull julia@sha256:0955c5756b87875173c9a5b65b2df8cbb7d5b390c9c4550f7f521c40b3fa1935
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2330962381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef0a0692cd89c0ebd705bcc2f6c2ddf0fa8c2f800111fbf1041ec324ce62832a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Thu, 15 Feb 2024 02:05:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 15 Feb 2024 02:05:41 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 02:05:42 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.1-win64.exe
# Thu, 15 Feb 2024 02:05:43 GMT
ENV JULIA_SHA256=ca02e6bd4f771d51c72520f359d727679775c03f62e7e7e2595dd79d1d0e5fec
# Thu, 15 Feb 2024 02:07:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 15 Feb 2024 02:07:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ed3e36144d60ff8117a3dd6eb64daa4e29953bb129aaad397b30092f9cc4c1`  
		Last Modified: Thu, 15 Feb 2024 02:07:25 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ff9d169a5e63801023c2b6a0a537977e5c7505d96e3c8896d7dfeadf1d0072`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948476976b5affd175205c3463e19547505c660c8d62ec0c51a0ccab24e7a100`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3066dd587e2e5fd44cc77bcf785a1eda6cb2c8fbfea705e112683712dc9bbf45`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de535d017baa9a7dbbcba70d7fde8cdb8607907fd1752fa99946ddf57958b2b0`  
		Last Modified: Thu, 15 Feb 2024 02:08:00 GMT  
		Size: 250.5 MB (250507125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1858c84143178e070fff903c762901603d1b1356e962f4fb73a71a200a55c84c`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-alpine`

```console
$ docker pull julia@sha256:38e9661d58c48669b03a2b9be0bb4c4fb995f270442388854bab380043c41e2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10-alpine` - linux; amd64

```console
$ docker pull julia@sha256:da0ebe0fdd8d2973c4cbe6c0b441739707a9173f47bf641dc5a0ded3e2d8ad4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.6 MB (177599522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4629a432942eac3a84338692a5217c4758a13da1e447a17b943a4ee5d0cf6357`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.1-musl-x86_64.tar.gz'; 			sha256='48e643c431f156e0cec440e3881f09dd78491c59de7804c73f470fba8cd64d1d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68eaf8cd85ce8bc2f83dd044858e77dc6ea04d797dcee4d4619f3a1dde5f73f1`  
		Last Modified: Thu, 15 Feb 2024 01:52:38 GMT  
		Size: 174.2 MB (174190425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e61b9b3f6995be6208e105dc44d9228d5bc22dc0570c34dbc7dfdd0dfb21b9e`  
		Last Modified: Thu, 15 Feb 2024 01:52:36 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-alpine` - unknown; unknown

```console
$ docker pull julia@sha256:07ab0484248a0b54bc9ccb67a15926fee6ecc1962552ddb0fc93651894af2a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.5 KB (119496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd5b516084ce3e9b080769c76191451657aab08f6d5bebe3ef5668280c39380`

```dockerfile
```

-	Layers:
	-	`sha256:ecaca48c94c6b70ef43edb0d3450d5d2d4cf2a5f5f18ef3b14326697c0a7c529`  
		Last Modified: Thu, 15 Feb 2024 01:52:36 GMT  
		Size: 104.8 KB (104799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bba9bd77ce2c5fd4ab756f06d5010801f772e290016bf8c6a1fc066d5c37d42`  
		Last Modified: Thu, 15 Feb 2024 01:52:36 GMT  
		Size: 14.7 KB (14697 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-alpine3.18`

```console
$ docker pull julia@sha256:4ec8fa66b1b062c5c7d0ce6c0796ba0c4ea4e5df6cfc03e43e30167e3eb30ad2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10-alpine3.18` - linux; amd64

```console
$ docker pull julia@sha256:e2e9526bf3bab718c84a9929115093953198eb43106374f04f9820f47c25997e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.6 MB (177593364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba54d9793c9d669939bcee642131032584105a0feaad52c06e388cf0d9e219b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.1-musl-x86_64.tar.gz'; 			sha256='48e643c431f156e0cec440e3881f09dd78491c59de7804c73f470fba8cd64d1d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=alpine&os_version=3.18"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef7909ee5233603cda10c2ca32601363045f0197c5f7ce5a3ab10251331176b`  
		Last Modified: Thu, 15 Feb 2024 01:52:50 GMT  
		Size: 174.2 MB (174190453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815110e9a9cb295a7eda0be2b78d3ce7016aa3a82d3d1b7791caf3bc003d9324`  
		Last Modified: Thu, 15 Feb 2024 01:52:47 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-alpine3.18` - unknown; unknown

```console
$ docker pull julia@sha256:7ae9f8f1ea5c2931c587ba63d2a8767bd35581eaf529e7390360469a88ec3434
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.5 KB (116519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df13cc1780fc7df1654365138f14d5147b21018d3a1d5f7238a0ac203b04b87e`

```dockerfile
```

-	Layers:
	-	`sha256:6fd0845ed3571a63743ec9da097c8e95cd1eb993e6cc66e605d7aaf438f3675a`  
		Last Modified: Thu, 15 Feb 2024 01:52:47 GMT  
		Size: 103.0 KB (103033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1393768754e0e0cd1f9f537f6a992341f9030f04e0e05217179713c8e4a0e4f`  
		Last Modified: Thu, 15 Feb 2024 01:52:47 GMT  
		Size: 13.5 KB (13486 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-alpine3.19`

```console
$ docker pull julia@sha256:38e9661d58c48669b03a2b9be0bb4c4fb995f270442388854bab380043c41e2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10-alpine3.19` - linux; amd64

```console
$ docker pull julia@sha256:da0ebe0fdd8d2973c4cbe6c0b441739707a9173f47bf641dc5a0ded3e2d8ad4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.6 MB (177599522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4629a432942eac3a84338692a5217c4758a13da1e447a17b943a4ee5d0cf6357`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.1-musl-x86_64.tar.gz'; 			sha256='48e643c431f156e0cec440e3881f09dd78491c59de7804c73f470fba8cd64d1d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68eaf8cd85ce8bc2f83dd044858e77dc6ea04d797dcee4d4619f3a1dde5f73f1`  
		Last Modified: Thu, 15 Feb 2024 01:52:38 GMT  
		Size: 174.2 MB (174190425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e61b9b3f6995be6208e105dc44d9228d5bc22dc0570c34dbc7dfdd0dfb21b9e`  
		Last Modified: Thu, 15 Feb 2024 01:52:36 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-alpine3.19` - unknown; unknown

```console
$ docker pull julia@sha256:07ab0484248a0b54bc9ccb67a15926fee6ecc1962552ddb0fc93651894af2a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.5 KB (119496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd5b516084ce3e9b080769c76191451657aab08f6d5bebe3ef5668280c39380`

```dockerfile
```

-	Layers:
	-	`sha256:ecaca48c94c6b70ef43edb0d3450d5d2d4cf2a5f5f18ef3b14326697c0a7c529`  
		Last Modified: Thu, 15 Feb 2024 01:52:36 GMT  
		Size: 104.8 KB (104799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bba9bd77ce2c5fd4ab756f06d5010801f772e290016bf8c6a1fc066d5c37d42`  
		Last Modified: Thu, 15 Feb 2024 01:52:36 GMT  
		Size: 14.7 KB (14697 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-bookworm`

```console
$ docker pull julia@sha256:687d51426b84545c07df8d8e90a6d40c8a9ecc6a4d1ec6143d3d8237a9d5d0dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.10-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:3caf5e0e4797801b5afa0cdb559075e1f7226c7ea16a3153fe7d18769aba94e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.2 MB (205223283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae4a5eea63105374a0e3ad6f704dedf7bf406350ddb98b6ad13582428fa24df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.1-linux-x86_64.tar.gz'; 			sha256='fe924258e55d074410b134195cf6b85cbe8f307fcd05a4fdd23f8944c5941a70'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.1-linux-aarch64.tar.gz'; 			sha256='67e912a2b8ae0fd2469a1a42c7d70b18cdf30b06dc717653fac64b710ca0575e'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.1-linux-i686.tar.gz'; 			sha256='46ae06f5690b4812e091f8e2a1b8a1caf849b5c842e8c7c3b8e474aaa7302526'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b760910a8ea7efbbc01dd05c522c09fbb768992e3e65929cf016f8a28e719d7`  
		Last Modified: Thu, 15 Feb 2024 01:52:52 GMT  
		Size: 5.7 MB (5707930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd429a837e23f6998e27565211ae302823134f3abdcf89d5a7c9400204139c55`  
		Last Modified: Thu, 15 Feb 2024 01:52:56 GMT  
		Size: 170.4 MB (170390890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6284bd0c80ca3e758d54e5f4f5076c25ccebccbba5d1108ef3ba6bc1703e73`  
		Last Modified: Thu, 15 Feb 2024 01:52:52 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:758cf0885b58460ec61796007b01d32c41f514dc0e1f8447e9a99f881f6666dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2158113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13bb7fc6510c67ceb8c7e7b0e22270d2ab6c904c71fc91de34003938191ebee1`

```dockerfile
```

-	Layers:
	-	`sha256:fe238e30162271ec796cf27837b3f1d078051f6979b4a0231cba428ae6598966`  
		Last Modified: Thu, 15 Feb 2024 01:52:52 GMT  
		Size: 2.1 MB (2139403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59fbd28bbcc24b3f7bb1c4f252a545a1236ff7692d9643ab5983bf53d2ef990b`  
		Last Modified: Thu, 15 Feb 2024 01:52:51 GMT  
		Size: 18.7 KB (18710 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:c7899893acb41c45312f7bcdc32512504b58ede63f02a0bba4dca92a272dbfda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.7 MB (199690181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:953f39f3ca0da48a4a5caebe30cc5d44769e6b518af75d4b51ce1f2b85fd7eaa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
CMD ["bash"]
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.1-linux-x86_64.tar.gz'; 			sha256='fe924258e55d074410b134195cf6b85cbe8f307fcd05a4fdd23f8944c5941a70'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.1-linux-aarch64.tar.gz'; 			sha256='67e912a2b8ae0fd2469a1a42c7d70b18cdf30b06dc717653fac64b710ca0575e'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.1-linux-i686.tar.gz'; 			sha256='46ae06f5690b4812e091f8e2a1b8a1caf849b5c842e8c7c3b8e474aaa7302526'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
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
	-	`sha256:df0a7047eef5296003128d4756f1f1b85b64c3f77206da6c62d958fc9572f10a`  
		Last Modified: Thu, 15 Feb 2024 02:14:07 GMT  
		Size: 165.0 MB (165000301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9f16d4c44b43675a53f7695a26f28e3cc7b16e7e71b0dddd82233834973fb3`  
		Last Modified: Thu, 15 Feb 2024 02:14:03 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:aaee047bc50ce902be26894ad0f4f267dda17086bf85430a1159a7ca679533de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2157334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c644ea6ef587504b4b31a9b2946c85895ec0a36586b46679c63753215cc4b8cd`

```dockerfile
```

-	Layers:
	-	`sha256:6ef921af30be56f765d798735060cdf175b864621010058e5c33ad36ac7a00b9`  
		Last Modified: Thu, 15 Feb 2024 02:14:03 GMT  
		Size: 2.1 MB (2138773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6bbf6d09ba5d03bb45cd1ca38605efef1b6f6227352ec90c0d7041a312e1e03`  
		Last Modified: Thu, 15 Feb 2024 02:14:03 GMT  
		Size: 18.6 KB (18561 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; 386

```console
$ docker pull julia@sha256:c733805bb2115e3e7ac2293646a60c5c37145d14575ae13a887543f7cfcfb120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192500887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27155dea2c1a627acfc854ba5afb07edabdbf706f1d74a0df905d2af1d98ace`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:56 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Tue, 13 Feb 2024 00:38:56 GMT
CMD ["bash"]
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.1-linux-x86_64.tar.gz'; 			sha256='fe924258e55d074410b134195cf6b85cbe8f307fcd05a4fdd23f8944c5941a70'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.1-linux-aarch64.tar.gz'; 			sha256='67e912a2b8ae0fd2469a1a42c7d70b18cdf30b06dc717653fac64b710ca0575e'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.1-linux-i686.tar.gz'; 			sha256='46ae06f5690b4812e091f8e2a1b8a1caf849b5c842e8c7c3b8e474aaa7302526'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b060bee81687c0dd068e9e9bb305e7d29ed2e3599f2ad66b28f8b70956a9fd21`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 5.9 MB (5863219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0a9393e3d7ec1e1d267186dd2e07326e97b56b875a4bb284b88b54504d9121`  
		Last Modified: Thu, 15 Feb 2024 01:52:46 GMT  
		Size: 156.5 MB (156495490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28dd21637325ca9b78d6c7e0a451b94a842713f5d96b2dfe69077bd35f7b44f`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:1460d63336cc97e4810367a540f40251647c57e6c86390c26469cf7da2b54930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2155240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4e048bdbabc6b4032e5cab36750926cf4d48be404b13f1d86268c55af218916`

```dockerfile
```

-	Layers:
	-	`sha256:0c29468e89b817688be1fa9de743c5e24910501b2881091894d40e5e6a71c2cb`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 2.1 MB (2136581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdd8305c04fcac3daa8caffcbcc79c942a6871f59a617792ec7e5741cc95c75b`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 18.7 KB (18659 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-bullseye`

```console
$ docker pull julia@sha256:7ad8dfad6efa322a660d6dd97a4f51d593e5ca3af248a8a10b07536169c13d28
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
$ docker pull julia@sha256:24c742c0cc59e688cca2b4064189e37ed35878c7f1709a2cffa3c8d89d64ddc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.2 MB (204239761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a882b29e497eb3cbd9ee464ae98d65cf2af1741338cc88dd8761fada5fb008`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.1-linux-x86_64.tar.gz'; 			sha256='fe924258e55d074410b134195cf6b85cbe8f307fcd05a4fdd23f8944c5941a70'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.1-linux-aarch64.tar.gz'; 			sha256='67e912a2b8ae0fd2469a1a42c7d70b18cdf30b06dc717653fac64b710ca0575e'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.1-linux-i686.tar.gz'; 			sha256='46ae06f5690b4812e091f8e2a1b8a1caf849b5c842e8c7c3b8e474aaa7302526'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52994ac9c626986c541c9af48e43ce1e0640e1923e36e90f5d0fac837147ce4f`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 2.4 MB (2426548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2953fea1f932882e3271c8cb61836952f6f90cfbaa344e8986500308c0cfe350`  
		Last Modified: Thu, 15 Feb 2024 01:52:45 GMT  
		Size: 170.4 MB (170390420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ddfead841b8c9404e76dd94b0b7a2340f8535ae2519d8fadfd50f6910a3b50a`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:2d799f94368b3ce51d7c73df4f866409c4274bbdd86f24af6604befc903ff1a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f294f1fdee6ae56922f01b720082730221f68e19fb7128cd6b956ec44ef36124`

```dockerfile
```

-	Layers:
	-	`sha256:74f859ebca0253d35bc9e06a1902608fa6958f913875dd6c9c4332601900ef57`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 2.4 MB (2359909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b86568a9b88e5470630bc40bf42cf53d203c35ff5d496a57d2f38fc9565de2c`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 17.5 KB (17540 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:99a7a3642824f780c5063e3332f761b4254397660f29b86033ee0c76042d8c42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.5 MB (197487223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e371987ac33efcf3b92b1e37091a25ce5adf8792a55f6670ffdf9ae1217acb3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.1-linux-x86_64.tar.gz'; 			sha256='fe924258e55d074410b134195cf6b85cbe8f307fcd05a4fdd23f8944c5941a70'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.1-linux-aarch64.tar.gz'; 			sha256='67e912a2b8ae0fd2469a1a42c7d70b18cdf30b06dc717653fac64b710ca0575e'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.1-linux-i686.tar.gz'; 			sha256='46ae06f5690b4812e091f8e2a1b8a1caf849b5c842e8c7c3b8e474aaa7302526'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
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
	-	`sha256:4fdc35222d7fcab46d11964d7e268775a9e4dbeebda85291a301ed8e3f38f12d`  
		Last Modified: Thu, 15 Feb 2024 02:15:10 GMT  
		Size: 165.0 MB (165000735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad69da563be9c7b3dc8b611885665f62220ebe6398e81be8b290f77b0269b90`  
		Last Modified: Thu, 15 Feb 2024 02:15:07 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:b8ff89e6d9cbd111de03fc482476ae6906c3e816120f66197e3238d29dd1f98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2376644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0a75eebe54c1ec99e9c01002195b63a859a0886f69df77d25e26c0ea55014bd`

```dockerfile
```

-	Layers:
	-	`sha256:8dc77e10839b1fb9c0dec75843295adca36d084e87b48ada981a892c3778d312`  
		Last Modified: Thu, 15 Feb 2024 02:15:06 GMT  
		Size: 2.4 MB (2359261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18b6801e86d58f2bb78f3906b735cd5539178e9c21fcfaeea7db87c57d3d825b`  
		Last Modified: Thu, 15 Feb 2024 02:15:06 GMT  
		Size: 17.4 KB (17383 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bullseye` - linux; 386

```console
$ docker pull julia@sha256:4cc3e8cc1fc2445d3c8958223fb7ff3ed7386fcc59053b4fbb52caa0b8b135f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191436740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a89c723882a8e89f126a53b96a86330d39b04f7fd394adb5be01967629f4a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:18 GMT
ADD file:9eaee5af136d095dc1dac0ffce0fde09d8f1bd02ff7cb65ee67e00b2a66f34f7 in / 
# Tue, 13 Feb 2024 00:39:19 GMT
CMD ["bash"]
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.1-linux-x86_64.tar.gz'; 			sha256='fe924258e55d074410b134195cf6b85cbe8f307fcd05a4fdd23f8944c5941a70'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.1-linux-aarch64.tar.gz'; 			sha256='67e912a2b8ae0fd2469a1a42c7d70b18cdf30b06dc717653fac64b710ca0575e'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.1-linux-i686.tar.gz'; 			sha256='46ae06f5690b4812e091f8e2a1b8a1caf849b5c842e8c7c3b8e474aaa7302526'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1ac8173b08d16f9f136fb0e3ee39999cef7495f924ecb43f3ca4a4eea267cc88`  
		Last Modified: Tue, 13 Feb 2024 00:44:36 GMT  
		Size: 32.4 MB (32407443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c2a21aba0b258d2d59ed768ff41751fcc88255368a239a0c26c72579e241ac`  
		Last Modified: Thu, 15 Feb 2024 01:52:40 GMT  
		Size: 2.5 MB (2533021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d246a08907e76876dc75135451dddc888bc48ceee300a8336e3172f79d0d246`  
		Last Modified: Thu, 15 Feb 2024 01:52:44 GMT  
		Size: 156.5 MB (156495904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45acd41394aa2be9e84237ed4d84fb4b41efa03ffdae3fee7ffe23d93fcc587f`  
		Last Modified: Thu, 15 Feb 2024 01:52:40 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:f324c95527f73df472f020fe9ad52ca74da2c87ea065cfc19eecf21d5d5ee350
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2374624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da94324fe8ee54c3188af2712264ee35eb43fcfbd1ffcfaff78c507270b0b33`

```dockerfile
```

-	Layers:
	-	`sha256:cbf974f51c72a3dabef9dfde0558dc77052a511c4f7b23f57744ad1d82a71698`  
		Last Modified: Thu, 15 Feb 2024 01:52:40 GMT  
		Size: 2.4 MB (2357115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44c5e6153327499afffa4e26339c505637b4ed975cb6175112ad50d21df77e8d`  
		Last Modified: Thu, 15 Feb 2024 01:52:40 GMT  
		Size: 17.5 KB (17509 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-windowsservercore`

```console
$ docker pull julia@sha256:91949f9dc6a2ba335f38712cd941eb739d1c64a260fde1059319857eab40e0e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

### `julia:1.10-windowsservercore` - windows version 10.0.20348.2322; amd64

```console
$ docker pull julia@sha256:ac7e7de1919e6a391278fd06062034d24dd1892f6569260439ea7a8aac745dd0
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2161166383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f26f77914b415046af8c139841e565707106b2048fc516c6c1cb8347d2a4f8`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Thu, 15 Feb 2024 01:55:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 15 Feb 2024 01:55:58 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 01:55:58 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.1-win64.exe
# Thu, 15 Feb 2024 01:55:59 GMT
ENV JULIA_SHA256=ca02e6bd4f771d51c72520f359d727679775c03f62e7e7e2595dd79d1d0e5fec
# Thu, 15 Feb 2024 01:57:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 15 Feb 2024 01:57:04 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ecd8f02f1b59d6f3aec1c570f2c8128d2b064a59e0da86653fdee442a472ad`  
		Last Modified: Thu, 15 Feb 2024 01:57:11 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62852f81701e842eaa34fb5baf41629e3a8bd717a09aeae6c9d8f85aa6d3d870`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a1387c2ad061bd6ecc5941ab04b037b84018b2bfddaa265150d148ffca73b4`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f3360ff5dce5375b4b898a4f4deb9f588e12659cb8db5611d7e3e01952b012`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44ebaee761d2302e12dcc0f6dc0d9e5debeb07658857a8749c1f96a07fa3bfb`  
		Last Modified: Thu, 15 Feb 2024 01:58:16 GMT  
		Size: 250.5 MB (250505768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c23a6fdc0fc3d51f4f3676cdf3a438f7d52cb9f9a6a964c4645f304cf900ff`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10-windowsservercore` - windows version 10.0.17763.5458; amd64

```console
$ docker pull julia@sha256:0955c5756b87875173c9a5b65b2df8cbb7d5b390c9c4550f7f521c40b3fa1935
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2330962381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef0a0692cd89c0ebd705bcc2f6c2ddf0fa8c2f800111fbf1041ec324ce62832a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Thu, 15 Feb 2024 02:05:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 15 Feb 2024 02:05:41 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 02:05:42 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.1-win64.exe
# Thu, 15 Feb 2024 02:05:43 GMT
ENV JULIA_SHA256=ca02e6bd4f771d51c72520f359d727679775c03f62e7e7e2595dd79d1d0e5fec
# Thu, 15 Feb 2024 02:07:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 15 Feb 2024 02:07:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ed3e36144d60ff8117a3dd6eb64daa4e29953bb129aaad397b30092f9cc4c1`  
		Last Modified: Thu, 15 Feb 2024 02:07:25 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ff9d169a5e63801023c2b6a0a537977e5c7505d96e3c8896d7dfeadf1d0072`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948476976b5affd175205c3463e19547505c660c8d62ec0c51a0ccab24e7a100`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3066dd587e2e5fd44cc77bcf785a1eda6cb2c8fbfea705e112683712dc9bbf45`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de535d017baa9a7dbbcba70d7fde8cdb8607907fd1752fa99946ddf57958b2b0`  
		Last Modified: Thu, 15 Feb 2024 02:08:00 GMT  
		Size: 250.5 MB (250507125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1858c84143178e070fff903c762901603d1b1356e962f4fb73a71a200a55c84c`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-windowsservercore-1809`

```console
$ docker pull julia@sha256:8720bbebce56e70f307b6ac3cd3d43e9f56b62fb168aade64cdb8abadc92f745
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `julia:1.10-windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull julia@sha256:0955c5756b87875173c9a5b65b2df8cbb7d5b390c9c4550f7f521c40b3fa1935
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2330962381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef0a0692cd89c0ebd705bcc2f6c2ddf0fa8c2f800111fbf1041ec324ce62832a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Thu, 15 Feb 2024 02:05:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 15 Feb 2024 02:05:41 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 02:05:42 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.1-win64.exe
# Thu, 15 Feb 2024 02:05:43 GMT
ENV JULIA_SHA256=ca02e6bd4f771d51c72520f359d727679775c03f62e7e7e2595dd79d1d0e5fec
# Thu, 15 Feb 2024 02:07:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 15 Feb 2024 02:07:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ed3e36144d60ff8117a3dd6eb64daa4e29953bb129aaad397b30092f9cc4c1`  
		Last Modified: Thu, 15 Feb 2024 02:07:25 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ff9d169a5e63801023c2b6a0a537977e5c7505d96e3c8896d7dfeadf1d0072`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948476976b5affd175205c3463e19547505c660c8d62ec0c51a0ccab24e7a100`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3066dd587e2e5fd44cc77bcf785a1eda6cb2c8fbfea705e112683712dc9bbf45`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de535d017baa9a7dbbcba70d7fde8cdb8607907fd1752fa99946ddf57958b2b0`  
		Last Modified: Thu, 15 Feb 2024 02:08:00 GMT  
		Size: 250.5 MB (250507125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1858c84143178e070fff903c762901603d1b1356e962f4fb73a71a200a55c84c`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:9a0e4ffc6087aabba7828052356da4cfbfb1db8f47eba6afec0c6bf93a96f3a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2322; amd64

### `julia:1.10-windowsservercore-ltsc2022` - windows version 10.0.20348.2322; amd64

```console
$ docker pull julia@sha256:ac7e7de1919e6a391278fd06062034d24dd1892f6569260439ea7a8aac745dd0
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2161166383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f26f77914b415046af8c139841e565707106b2048fc516c6c1cb8347d2a4f8`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Thu, 15 Feb 2024 01:55:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 15 Feb 2024 01:55:58 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 01:55:58 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.1-win64.exe
# Thu, 15 Feb 2024 01:55:59 GMT
ENV JULIA_SHA256=ca02e6bd4f771d51c72520f359d727679775c03f62e7e7e2595dd79d1d0e5fec
# Thu, 15 Feb 2024 01:57:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 15 Feb 2024 01:57:04 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ecd8f02f1b59d6f3aec1c570f2c8128d2b064a59e0da86653fdee442a472ad`  
		Last Modified: Thu, 15 Feb 2024 01:57:11 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62852f81701e842eaa34fb5baf41629e3a8bd717a09aeae6c9d8f85aa6d3d870`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a1387c2ad061bd6ecc5941ab04b037b84018b2bfddaa265150d148ffca73b4`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f3360ff5dce5375b4b898a4f4deb9f588e12659cb8db5611d7e3e01952b012`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44ebaee761d2302e12dcc0f6dc0d9e5debeb07658857a8749c1f96a07fa3bfb`  
		Last Modified: Thu, 15 Feb 2024 01:58:16 GMT  
		Size: 250.5 MB (250505768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c23a6fdc0fc3d51f4f3676cdf3a438f7d52cb9f9a6a964c4645f304cf900ff`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.1`

```console
$ docker pull julia@sha256:2d992bcdfd817a11bfa70918879674b62dcd0a497e079116605c33dc9979589e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

### `julia:1.10.1` - linux; amd64

```console
$ docker pull julia@sha256:3caf5e0e4797801b5afa0cdb559075e1f7226c7ea16a3153fe7d18769aba94e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.2 MB (205223283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae4a5eea63105374a0e3ad6f704dedf7bf406350ddb98b6ad13582428fa24df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.1-linux-x86_64.tar.gz'; 			sha256='fe924258e55d074410b134195cf6b85cbe8f307fcd05a4fdd23f8944c5941a70'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.1-linux-aarch64.tar.gz'; 			sha256='67e912a2b8ae0fd2469a1a42c7d70b18cdf30b06dc717653fac64b710ca0575e'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.1-linux-i686.tar.gz'; 			sha256='46ae06f5690b4812e091f8e2a1b8a1caf849b5c842e8c7c3b8e474aaa7302526'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b760910a8ea7efbbc01dd05c522c09fbb768992e3e65929cf016f8a28e719d7`  
		Last Modified: Thu, 15 Feb 2024 01:52:52 GMT  
		Size: 5.7 MB (5707930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd429a837e23f6998e27565211ae302823134f3abdcf89d5a7c9400204139c55`  
		Last Modified: Thu, 15 Feb 2024 01:52:56 GMT  
		Size: 170.4 MB (170390890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6284bd0c80ca3e758d54e5f4f5076c25ccebccbba5d1108ef3ba6bc1703e73`  
		Last Modified: Thu, 15 Feb 2024 01:52:52 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.1` - unknown; unknown

```console
$ docker pull julia@sha256:758cf0885b58460ec61796007b01d32c41f514dc0e1f8447e9a99f881f6666dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2158113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13bb7fc6510c67ceb8c7e7b0e22270d2ab6c904c71fc91de34003938191ebee1`

```dockerfile
```

-	Layers:
	-	`sha256:fe238e30162271ec796cf27837b3f1d078051f6979b4a0231cba428ae6598966`  
		Last Modified: Thu, 15 Feb 2024 01:52:52 GMT  
		Size: 2.1 MB (2139403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59fbd28bbcc24b3f7bb1c4f252a545a1236ff7692d9643ab5983bf53d2ef990b`  
		Last Modified: Thu, 15 Feb 2024 01:52:51 GMT  
		Size: 18.7 KB (18710 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.1` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:c7899893acb41c45312f7bcdc32512504b58ede63f02a0bba4dca92a272dbfda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.7 MB (199690181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:953f39f3ca0da48a4a5caebe30cc5d44769e6b518af75d4b51ce1f2b85fd7eaa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
CMD ["bash"]
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.1-linux-x86_64.tar.gz'; 			sha256='fe924258e55d074410b134195cf6b85cbe8f307fcd05a4fdd23f8944c5941a70'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.1-linux-aarch64.tar.gz'; 			sha256='67e912a2b8ae0fd2469a1a42c7d70b18cdf30b06dc717653fac64b710ca0575e'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.1-linux-i686.tar.gz'; 			sha256='46ae06f5690b4812e091f8e2a1b8a1caf849b5c842e8c7c3b8e474aaa7302526'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
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
	-	`sha256:df0a7047eef5296003128d4756f1f1b85b64c3f77206da6c62d958fc9572f10a`  
		Last Modified: Thu, 15 Feb 2024 02:14:07 GMT  
		Size: 165.0 MB (165000301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9f16d4c44b43675a53f7695a26f28e3cc7b16e7e71b0dddd82233834973fb3`  
		Last Modified: Thu, 15 Feb 2024 02:14:03 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.1` - unknown; unknown

```console
$ docker pull julia@sha256:aaee047bc50ce902be26894ad0f4f267dda17086bf85430a1159a7ca679533de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2157334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c644ea6ef587504b4b31a9b2946c85895ec0a36586b46679c63753215cc4b8cd`

```dockerfile
```

-	Layers:
	-	`sha256:6ef921af30be56f765d798735060cdf175b864621010058e5c33ad36ac7a00b9`  
		Last Modified: Thu, 15 Feb 2024 02:14:03 GMT  
		Size: 2.1 MB (2138773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6bbf6d09ba5d03bb45cd1ca38605efef1b6f6227352ec90c0d7041a312e1e03`  
		Last Modified: Thu, 15 Feb 2024 02:14:03 GMT  
		Size: 18.6 KB (18561 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.1` - linux; 386

```console
$ docker pull julia@sha256:c733805bb2115e3e7ac2293646a60c5c37145d14575ae13a887543f7cfcfb120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192500887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27155dea2c1a627acfc854ba5afb07edabdbf706f1d74a0df905d2af1d98ace`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:56 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Tue, 13 Feb 2024 00:38:56 GMT
CMD ["bash"]
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.1-linux-x86_64.tar.gz'; 			sha256='fe924258e55d074410b134195cf6b85cbe8f307fcd05a4fdd23f8944c5941a70'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.1-linux-aarch64.tar.gz'; 			sha256='67e912a2b8ae0fd2469a1a42c7d70b18cdf30b06dc717653fac64b710ca0575e'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.1-linux-i686.tar.gz'; 			sha256='46ae06f5690b4812e091f8e2a1b8a1caf849b5c842e8c7c3b8e474aaa7302526'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b060bee81687c0dd068e9e9bb305e7d29ed2e3599f2ad66b28f8b70956a9fd21`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 5.9 MB (5863219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0a9393e3d7ec1e1d267186dd2e07326e97b56b875a4bb284b88b54504d9121`  
		Last Modified: Thu, 15 Feb 2024 01:52:46 GMT  
		Size: 156.5 MB (156495490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28dd21637325ca9b78d6c7e0a451b94a842713f5d96b2dfe69077bd35f7b44f`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.1` - unknown; unknown

```console
$ docker pull julia@sha256:1460d63336cc97e4810367a540f40251647c57e6c86390c26469cf7da2b54930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2155240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4e048bdbabc6b4032e5cab36750926cf4d48be404b13f1d86268c55af218916`

```dockerfile
```

-	Layers:
	-	`sha256:0c29468e89b817688be1fa9de743c5e24910501b2881091894d40e5e6a71c2cb`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 2.1 MB (2136581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdd8305c04fcac3daa8caffcbcc79c942a6871f59a617792ec7e5741cc95c75b`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 18.7 KB (18659 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.1` - windows version 10.0.20348.2322; amd64

```console
$ docker pull julia@sha256:ac7e7de1919e6a391278fd06062034d24dd1892f6569260439ea7a8aac745dd0
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2161166383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f26f77914b415046af8c139841e565707106b2048fc516c6c1cb8347d2a4f8`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Thu, 15 Feb 2024 01:55:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 15 Feb 2024 01:55:58 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 01:55:58 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.1-win64.exe
# Thu, 15 Feb 2024 01:55:59 GMT
ENV JULIA_SHA256=ca02e6bd4f771d51c72520f359d727679775c03f62e7e7e2595dd79d1d0e5fec
# Thu, 15 Feb 2024 01:57:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 15 Feb 2024 01:57:04 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ecd8f02f1b59d6f3aec1c570f2c8128d2b064a59e0da86653fdee442a472ad`  
		Last Modified: Thu, 15 Feb 2024 01:57:11 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62852f81701e842eaa34fb5baf41629e3a8bd717a09aeae6c9d8f85aa6d3d870`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a1387c2ad061bd6ecc5941ab04b037b84018b2bfddaa265150d148ffca73b4`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f3360ff5dce5375b4b898a4f4deb9f588e12659cb8db5611d7e3e01952b012`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44ebaee761d2302e12dcc0f6dc0d9e5debeb07658857a8749c1f96a07fa3bfb`  
		Last Modified: Thu, 15 Feb 2024 01:58:16 GMT  
		Size: 250.5 MB (250505768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c23a6fdc0fc3d51f4f3676cdf3a438f7d52cb9f9a6a964c4645f304cf900ff`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10.1` - windows version 10.0.17763.5458; amd64

```console
$ docker pull julia@sha256:0955c5756b87875173c9a5b65b2df8cbb7d5b390c9c4550f7f521c40b3fa1935
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2330962381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef0a0692cd89c0ebd705bcc2f6c2ddf0fa8c2f800111fbf1041ec324ce62832a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Thu, 15 Feb 2024 02:05:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 15 Feb 2024 02:05:41 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 02:05:42 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.1-win64.exe
# Thu, 15 Feb 2024 02:05:43 GMT
ENV JULIA_SHA256=ca02e6bd4f771d51c72520f359d727679775c03f62e7e7e2595dd79d1d0e5fec
# Thu, 15 Feb 2024 02:07:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 15 Feb 2024 02:07:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ed3e36144d60ff8117a3dd6eb64daa4e29953bb129aaad397b30092f9cc4c1`  
		Last Modified: Thu, 15 Feb 2024 02:07:25 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ff9d169a5e63801023c2b6a0a537977e5c7505d96e3c8896d7dfeadf1d0072`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948476976b5affd175205c3463e19547505c660c8d62ec0c51a0ccab24e7a100`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3066dd587e2e5fd44cc77bcf785a1eda6cb2c8fbfea705e112683712dc9bbf45`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de535d017baa9a7dbbcba70d7fde8cdb8607907fd1752fa99946ddf57958b2b0`  
		Last Modified: Thu, 15 Feb 2024 02:08:00 GMT  
		Size: 250.5 MB (250507125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1858c84143178e070fff903c762901603d1b1356e962f4fb73a71a200a55c84c`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.1-alpine`

```console
$ docker pull julia@sha256:38e9661d58c48669b03a2b9be0bb4c4fb995f270442388854bab380043c41e2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10.1-alpine` - linux; amd64

```console
$ docker pull julia@sha256:da0ebe0fdd8d2973c4cbe6c0b441739707a9173f47bf641dc5a0ded3e2d8ad4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.6 MB (177599522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4629a432942eac3a84338692a5217c4758a13da1e447a17b943a4ee5d0cf6357`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.1-musl-x86_64.tar.gz'; 			sha256='48e643c431f156e0cec440e3881f09dd78491c59de7804c73f470fba8cd64d1d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68eaf8cd85ce8bc2f83dd044858e77dc6ea04d797dcee4d4619f3a1dde5f73f1`  
		Last Modified: Thu, 15 Feb 2024 01:52:38 GMT  
		Size: 174.2 MB (174190425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e61b9b3f6995be6208e105dc44d9228d5bc22dc0570c34dbc7dfdd0dfb21b9e`  
		Last Modified: Thu, 15 Feb 2024 01:52:36 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.1-alpine` - unknown; unknown

```console
$ docker pull julia@sha256:07ab0484248a0b54bc9ccb67a15926fee6ecc1962552ddb0fc93651894af2a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.5 KB (119496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd5b516084ce3e9b080769c76191451657aab08f6d5bebe3ef5668280c39380`

```dockerfile
```

-	Layers:
	-	`sha256:ecaca48c94c6b70ef43edb0d3450d5d2d4cf2a5f5f18ef3b14326697c0a7c529`  
		Last Modified: Thu, 15 Feb 2024 01:52:36 GMT  
		Size: 104.8 KB (104799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bba9bd77ce2c5fd4ab756f06d5010801f772e290016bf8c6a1fc066d5c37d42`  
		Last Modified: Thu, 15 Feb 2024 01:52:36 GMT  
		Size: 14.7 KB (14697 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.1-alpine3.18`

```console
$ docker pull julia@sha256:4ec8fa66b1b062c5c7d0ce6c0796ba0c4ea4e5df6cfc03e43e30167e3eb30ad2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10.1-alpine3.18` - linux; amd64

```console
$ docker pull julia@sha256:e2e9526bf3bab718c84a9929115093953198eb43106374f04f9820f47c25997e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.6 MB (177593364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba54d9793c9d669939bcee642131032584105a0feaad52c06e388cf0d9e219b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.1-musl-x86_64.tar.gz'; 			sha256='48e643c431f156e0cec440e3881f09dd78491c59de7804c73f470fba8cd64d1d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=alpine&os_version=3.18"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef7909ee5233603cda10c2ca32601363045f0197c5f7ce5a3ab10251331176b`  
		Last Modified: Thu, 15 Feb 2024 01:52:50 GMT  
		Size: 174.2 MB (174190453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815110e9a9cb295a7eda0be2b78d3ce7016aa3a82d3d1b7791caf3bc003d9324`  
		Last Modified: Thu, 15 Feb 2024 01:52:47 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.1-alpine3.18` - unknown; unknown

```console
$ docker pull julia@sha256:7ae9f8f1ea5c2931c587ba63d2a8767bd35581eaf529e7390360469a88ec3434
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.5 KB (116519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df13cc1780fc7df1654365138f14d5147b21018d3a1d5f7238a0ac203b04b87e`

```dockerfile
```

-	Layers:
	-	`sha256:6fd0845ed3571a63743ec9da097c8e95cd1eb993e6cc66e605d7aaf438f3675a`  
		Last Modified: Thu, 15 Feb 2024 01:52:47 GMT  
		Size: 103.0 KB (103033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1393768754e0e0cd1f9f537f6a992341f9030f04e0e05217179713c8e4a0e4f`  
		Last Modified: Thu, 15 Feb 2024 01:52:47 GMT  
		Size: 13.5 KB (13486 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.1-alpine3.19`

```console
$ docker pull julia@sha256:38e9661d58c48669b03a2b9be0bb4c4fb995f270442388854bab380043c41e2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10.1-alpine3.19` - linux; amd64

```console
$ docker pull julia@sha256:da0ebe0fdd8d2973c4cbe6c0b441739707a9173f47bf641dc5a0ded3e2d8ad4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.6 MB (177599522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4629a432942eac3a84338692a5217c4758a13da1e447a17b943a4ee5d0cf6357`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.1-musl-x86_64.tar.gz'; 			sha256='48e643c431f156e0cec440e3881f09dd78491c59de7804c73f470fba8cd64d1d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68eaf8cd85ce8bc2f83dd044858e77dc6ea04d797dcee4d4619f3a1dde5f73f1`  
		Last Modified: Thu, 15 Feb 2024 01:52:38 GMT  
		Size: 174.2 MB (174190425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e61b9b3f6995be6208e105dc44d9228d5bc22dc0570c34dbc7dfdd0dfb21b9e`  
		Last Modified: Thu, 15 Feb 2024 01:52:36 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.1-alpine3.19` - unknown; unknown

```console
$ docker pull julia@sha256:07ab0484248a0b54bc9ccb67a15926fee6ecc1962552ddb0fc93651894af2a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.5 KB (119496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd5b516084ce3e9b080769c76191451657aab08f6d5bebe3ef5668280c39380`

```dockerfile
```

-	Layers:
	-	`sha256:ecaca48c94c6b70ef43edb0d3450d5d2d4cf2a5f5f18ef3b14326697c0a7c529`  
		Last Modified: Thu, 15 Feb 2024 01:52:36 GMT  
		Size: 104.8 KB (104799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bba9bd77ce2c5fd4ab756f06d5010801f772e290016bf8c6a1fc066d5c37d42`  
		Last Modified: Thu, 15 Feb 2024 01:52:36 GMT  
		Size: 14.7 KB (14697 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.1-bookworm`

```console
$ docker pull julia@sha256:687d51426b84545c07df8d8e90a6d40c8a9ecc6a4d1ec6143d3d8237a9d5d0dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.10.1-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:3caf5e0e4797801b5afa0cdb559075e1f7226c7ea16a3153fe7d18769aba94e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.2 MB (205223283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae4a5eea63105374a0e3ad6f704dedf7bf406350ddb98b6ad13582428fa24df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.1-linux-x86_64.tar.gz'; 			sha256='fe924258e55d074410b134195cf6b85cbe8f307fcd05a4fdd23f8944c5941a70'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.1-linux-aarch64.tar.gz'; 			sha256='67e912a2b8ae0fd2469a1a42c7d70b18cdf30b06dc717653fac64b710ca0575e'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.1-linux-i686.tar.gz'; 			sha256='46ae06f5690b4812e091f8e2a1b8a1caf849b5c842e8c7c3b8e474aaa7302526'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b760910a8ea7efbbc01dd05c522c09fbb768992e3e65929cf016f8a28e719d7`  
		Last Modified: Thu, 15 Feb 2024 01:52:52 GMT  
		Size: 5.7 MB (5707930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd429a837e23f6998e27565211ae302823134f3abdcf89d5a7c9400204139c55`  
		Last Modified: Thu, 15 Feb 2024 01:52:56 GMT  
		Size: 170.4 MB (170390890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6284bd0c80ca3e758d54e5f4f5076c25ccebccbba5d1108ef3ba6bc1703e73`  
		Last Modified: Thu, 15 Feb 2024 01:52:52 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:758cf0885b58460ec61796007b01d32c41f514dc0e1f8447e9a99f881f6666dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2158113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13bb7fc6510c67ceb8c7e7b0e22270d2ab6c904c71fc91de34003938191ebee1`

```dockerfile
```

-	Layers:
	-	`sha256:fe238e30162271ec796cf27837b3f1d078051f6979b4a0231cba428ae6598966`  
		Last Modified: Thu, 15 Feb 2024 01:52:52 GMT  
		Size: 2.1 MB (2139403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59fbd28bbcc24b3f7bb1c4f252a545a1236ff7692d9643ab5983bf53d2ef990b`  
		Last Modified: Thu, 15 Feb 2024 01:52:51 GMT  
		Size: 18.7 KB (18710 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.1-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:c7899893acb41c45312f7bcdc32512504b58ede63f02a0bba4dca92a272dbfda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.7 MB (199690181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:953f39f3ca0da48a4a5caebe30cc5d44769e6b518af75d4b51ce1f2b85fd7eaa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
CMD ["bash"]
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.1-linux-x86_64.tar.gz'; 			sha256='fe924258e55d074410b134195cf6b85cbe8f307fcd05a4fdd23f8944c5941a70'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.1-linux-aarch64.tar.gz'; 			sha256='67e912a2b8ae0fd2469a1a42c7d70b18cdf30b06dc717653fac64b710ca0575e'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.1-linux-i686.tar.gz'; 			sha256='46ae06f5690b4812e091f8e2a1b8a1caf849b5c842e8c7c3b8e474aaa7302526'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
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
	-	`sha256:df0a7047eef5296003128d4756f1f1b85b64c3f77206da6c62d958fc9572f10a`  
		Last Modified: Thu, 15 Feb 2024 02:14:07 GMT  
		Size: 165.0 MB (165000301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9f16d4c44b43675a53f7695a26f28e3cc7b16e7e71b0dddd82233834973fb3`  
		Last Modified: Thu, 15 Feb 2024 02:14:03 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:aaee047bc50ce902be26894ad0f4f267dda17086bf85430a1159a7ca679533de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2157334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c644ea6ef587504b4b31a9b2946c85895ec0a36586b46679c63753215cc4b8cd`

```dockerfile
```

-	Layers:
	-	`sha256:6ef921af30be56f765d798735060cdf175b864621010058e5c33ad36ac7a00b9`  
		Last Modified: Thu, 15 Feb 2024 02:14:03 GMT  
		Size: 2.1 MB (2138773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6bbf6d09ba5d03bb45cd1ca38605efef1b6f6227352ec90c0d7041a312e1e03`  
		Last Modified: Thu, 15 Feb 2024 02:14:03 GMT  
		Size: 18.6 KB (18561 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.1-bookworm` - linux; 386

```console
$ docker pull julia@sha256:c733805bb2115e3e7ac2293646a60c5c37145d14575ae13a887543f7cfcfb120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192500887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27155dea2c1a627acfc854ba5afb07edabdbf706f1d74a0df905d2af1d98ace`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:56 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Tue, 13 Feb 2024 00:38:56 GMT
CMD ["bash"]
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.1-linux-x86_64.tar.gz'; 			sha256='fe924258e55d074410b134195cf6b85cbe8f307fcd05a4fdd23f8944c5941a70'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.1-linux-aarch64.tar.gz'; 			sha256='67e912a2b8ae0fd2469a1a42c7d70b18cdf30b06dc717653fac64b710ca0575e'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.1-linux-i686.tar.gz'; 			sha256='46ae06f5690b4812e091f8e2a1b8a1caf849b5c842e8c7c3b8e474aaa7302526'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b060bee81687c0dd068e9e9bb305e7d29ed2e3599f2ad66b28f8b70956a9fd21`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 5.9 MB (5863219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0a9393e3d7ec1e1d267186dd2e07326e97b56b875a4bb284b88b54504d9121`  
		Last Modified: Thu, 15 Feb 2024 01:52:46 GMT  
		Size: 156.5 MB (156495490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28dd21637325ca9b78d6c7e0a451b94a842713f5d96b2dfe69077bd35f7b44f`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:1460d63336cc97e4810367a540f40251647c57e6c86390c26469cf7da2b54930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2155240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4e048bdbabc6b4032e5cab36750926cf4d48be404b13f1d86268c55af218916`

```dockerfile
```

-	Layers:
	-	`sha256:0c29468e89b817688be1fa9de743c5e24910501b2881091894d40e5e6a71c2cb`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 2.1 MB (2136581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdd8305c04fcac3daa8caffcbcc79c942a6871f59a617792ec7e5741cc95c75b`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 18.7 KB (18659 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.1-bullseye`

```console
$ docker pull julia@sha256:7ad8dfad6efa322a660d6dd97a4f51d593e5ca3af248a8a10b07536169c13d28
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.10.1-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:24c742c0cc59e688cca2b4064189e37ed35878c7f1709a2cffa3c8d89d64ddc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.2 MB (204239761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a882b29e497eb3cbd9ee464ae98d65cf2af1741338cc88dd8761fada5fb008`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.1-linux-x86_64.tar.gz'; 			sha256='fe924258e55d074410b134195cf6b85cbe8f307fcd05a4fdd23f8944c5941a70'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.1-linux-aarch64.tar.gz'; 			sha256='67e912a2b8ae0fd2469a1a42c7d70b18cdf30b06dc717653fac64b710ca0575e'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.1-linux-i686.tar.gz'; 			sha256='46ae06f5690b4812e091f8e2a1b8a1caf849b5c842e8c7c3b8e474aaa7302526'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52994ac9c626986c541c9af48e43ce1e0640e1923e36e90f5d0fac837147ce4f`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 2.4 MB (2426548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2953fea1f932882e3271c8cb61836952f6f90cfbaa344e8986500308c0cfe350`  
		Last Modified: Thu, 15 Feb 2024 01:52:45 GMT  
		Size: 170.4 MB (170390420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ddfead841b8c9404e76dd94b0b7a2340f8535ae2519d8fadfd50f6910a3b50a`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:2d799f94368b3ce51d7c73df4f866409c4274bbdd86f24af6604befc903ff1a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f294f1fdee6ae56922f01b720082730221f68e19fb7128cd6b956ec44ef36124`

```dockerfile
```

-	Layers:
	-	`sha256:74f859ebca0253d35bc9e06a1902608fa6958f913875dd6c9c4332601900ef57`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 2.4 MB (2359909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b86568a9b88e5470630bc40bf42cf53d203c35ff5d496a57d2f38fc9565de2c`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 17.5 KB (17540 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.1-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:99a7a3642824f780c5063e3332f761b4254397660f29b86033ee0c76042d8c42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.5 MB (197487223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e371987ac33efcf3b92b1e37091a25ce5adf8792a55f6670ffdf9ae1217acb3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.1-linux-x86_64.tar.gz'; 			sha256='fe924258e55d074410b134195cf6b85cbe8f307fcd05a4fdd23f8944c5941a70'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.1-linux-aarch64.tar.gz'; 			sha256='67e912a2b8ae0fd2469a1a42c7d70b18cdf30b06dc717653fac64b710ca0575e'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.1-linux-i686.tar.gz'; 			sha256='46ae06f5690b4812e091f8e2a1b8a1caf849b5c842e8c7c3b8e474aaa7302526'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
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
	-	`sha256:4fdc35222d7fcab46d11964d7e268775a9e4dbeebda85291a301ed8e3f38f12d`  
		Last Modified: Thu, 15 Feb 2024 02:15:10 GMT  
		Size: 165.0 MB (165000735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad69da563be9c7b3dc8b611885665f62220ebe6398e81be8b290f77b0269b90`  
		Last Modified: Thu, 15 Feb 2024 02:15:07 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:b8ff89e6d9cbd111de03fc482476ae6906c3e816120f66197e3238d29dd1f98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2376644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0a75eebe54c1ec99e9c01002195b63a859a0886f69df77d25e26c0ea55014bd`

```dockerfile
```

-	Layers:
	-	`sha256:8dc77e10839b1fb9c0dec75843295adca36d084e87b48ada981a892c3778d312`  
		Last Modified: Thu, 15 Feb 2024 02:15:06 GMT  
		Size: 2.4 MB (2359261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18b6801e86d58f2bb78f3906b735cd5539178e9c21fcfaeea7db87c57d3d825b`  
		Last Modified: Thu, 15 Feb 2024 02:15:06 GMT  
		Size: 17.4 KB (17383 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.1-bullseye` - linux; 386

```console
$ docker pull julia@sha256:4cc3e8cc1fc2445d3c8958223fb7ff3ed7386fcc59053b4fbb52caa0b8b135f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191436740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a89c723882a8e89f126a53b96a86330d39b04f7fd394adb5be01967629f4a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:18 GMT
ADD file:9eaee5af136d095dc1dac0ffce0fde09d8f1bd02ff7cb65ee67e00b2a66f34f7 in / 
# Tue, 13 Feb 2024 00:39:19 GMT
CMD ["bash"]
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.1-linux-x86_64.tar.gz'; 			sha256='fe924258e55d074410b134195cf6b85cbe8f307fcd05a4fdd23f8944c5941a70'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.1-linux-aarch64.tar.gz'; 			sha256='67e912a2b8ae0fd2469a1a42c7d70b18cdf30b06dc717653fac64b710ca0575e'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.1-linux-i686.tar.gz'; 			sha256='46ae06f5690b4812e091f8e2a1b8a1caf849b5c842e8c7c3b8e474aaa7302526'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1ac8173b08d16f9f136fb0e3ee39999cef7495f924ecb43f3ca4a4eea267cc88`  
		Last Modified: Tue, 13 Feb 2024 00:44:36 GMT  
		Size: 32.4 MB (32407443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c2a21aba0b258d2d59ed768ff41751fcc88255368a239a0c26c72579e241ac`  
		Last Modified: Thu, 15 Feb 2024 01:52:40 GMT  
		Size: 2.5 MB (2533021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d246a08907e76876dc75135451dddc888bc48ceee300a8336e3172f79d0d246`  
		Last Modified: Thu, 15 Feb 2024 01:52:44 GMT  
		Size: 156.5 MB (156495904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45acd41394aa2be9e84237ed4d84fb4b41efa03ffdae3fee7ffe23d93fcc587f`  
		Last Modified: Thu, 15 Feb 2024 01:52:40 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:f324c95527f73df472f020fe9ad52ca74da2c87ea065cfc19eecf21d5d5ee350
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2374624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da94324fe8ee54c3188af2712264ee35eb43fcfbd1ffcfaff78c507270b0b33`

```dockerfile
```

-	Layers:
	-	`sha256:cbf974f51c72a3dabef9dfde0558dc77052a511c4f7b23f57744ad1d82a71698`  
		Last Modified: Thu, 15 Feb 2024 01:52:40 GMT  
		Size: 2.4 MB (2357115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44c5e6153327499afffa4e26339c505637b4ed975cb6175112ad50d21df77e8d`  
		Last Modified: Thu, 15 Feb 2024 01:52:40 GMT  
		Size: 17.5 KB (17509 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.1-windowsservercore`

```console
$ docker pull julia@sha256:91949f9dc6a2ba335f38712cd941eb739d1c64a260fde1059319857eab40e0e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

### `julia:1.10.1-windowsservercore` - windows version 10.0.20348.2322; amd64

```console
$ docker pull julia@sha256:ac7e7de1919e6a391278fd06062034d24dd1892f6569260439ea7a8aac745dd0
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2161166383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f26f77914b415046af8c139841e565707106b2048fc516c6c1cb8347d2a4f8`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Thu, 15 Feb 2024 01:55:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 15 Feb 2024 01:55:58 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 01:55:58 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.1-win64.exe
# Thu, 15 Feb 2024 01:55:59 GMT
ENV JULIA_SHA256=ca02e6bd4f771d51c72520f359d727679775c03f62e7e7e2595dd79d1d0e5fec
# Thu, 15 Feb 2024 01:57:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 15 Feb 2024 01:57:04 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ecd8f02f1b59d6f3aec1c570f2c8128d2b064a59e0da86653fdee442a472ad`  
		Last Modified: Thu, 15 Feb 2024 01:57:11 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62852f81701e842eaa34fb5baf41629e3a8bd717a09aeae6c9d8f85aa6d3d870`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a1387c2ad061bd6ecc5941ab04b037b84018b2bfddaa265150d148ffca73b4`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f3360ff5dce5375b4b898a4f4deb9f588e12659cb8db5611d7e3e01952b012`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44ebaee761d2302e12dcc0f6dc0d9e5debeb07658857a8749c1f96a07fa3bfb`  
		Last Modified: Thu, 15 Feb 2024 01:58:16 GMT  
		Size: 250.5 MB (250505768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c23a6fdc0fc3d51f4f3676cdf3a438f7d52cb9f9a6a964c4645f304cf900ff`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10.1-windowsservercore` - windows version 10.0.17763.5458; amd64

```console
$ docker pull julia@sha256:0955c5756b87875173c9a5b65b2df8cbb7d5b390c9c4550f7f521c40b3fa1935
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2330962381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef0a0692cd89c0ebd705bcc2f6c2ddf0fa8c2f800111fbf1041ec324ce62832a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Thu, 15 Feb 2024 02:05:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 15 Feb 2024 02:05:41 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 02:05:42 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.1-win64.exe
# Thu, 15 Feb 2024 02:05:43 GMT
ENV JULIA_SHA256=ca02e6bd4f771d51c72520f359d727679775c03f62e7e7e2595dd79d1d0e5fec
# Thu, 15 Feb 2024 02:07:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 15 Feb 2024 02:07:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ed3e36144d60ff8117a3dd6eb64daa4e29953bb129aaad397b30092f9cc4c1`  
		Last Modified: Thu, 15 Feb 2024 02:07:25 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ff9d169a5e63801023c2b6a0a537977e5c7505d96e3c8896d7dfeadf1d0072`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948476976b5affd175205c3463e19547505c660c8d62ec0c51a0ccab24e7a100`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3066dd587e2e5fd44cc77bcf785a1eda6cb2c8fbfea705e112683712dc9bbf45`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de535d017baa9a7dbbcba70d7fde8cdb8607907fd1752fa99946ddf57958b2b0`  
		Last Modified: Thu, 15 Feb 2024 02:08:00 GMT  
		Size: 250.5 MB (250507125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1858c84143178e070fff903c762901603d1b1356e962f4fb73a71a200a55c84c`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.1-windowsservercore-1809`

```console
$ docker pull julia@sha256:8720bbebce56e70f307b6ac3cd3d43e9f56b62fb168aade64cdb8abadc92f745
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `julia:1.10.1-windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull julia@sha256:0955c5756b87875173c9a5b65b2df8cbb7d5b390c9c4550f7f521c40b3fa1935
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2330962381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef0a0692cd89c0ebd705bcc2f6c2ddf0fa8c2f800111fbf1041ec324ce62832a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Thu, 15 Feb 2024 02:05:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 15 Feb 2024 02:05:41 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 02:05:42 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.1-win64.exe
# Thu, 15 Feb 2024 02:05:43 GMT
ENV JULIA_SHA256=ca02e6bd4f771d51c72520f359d727679775c03f62e7e7e2595dd79d1d0e5fec
# Thu, 15 Feb 2024 02:07:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 15 Feb 2024 02:07:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ed3e36144d60ff8117a3dd6eb64daa4e29953bb129aaad397b30092f9cc4c1`  
		Last Modified: Thu, 15 Feb 2024 02:07:25 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ff9d169a5e63801023c2b6a0a537977e5c7505d96e3c8896d7dfeadf1d0072`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948476976b5affd175205c3463e19547505c660c8d62ec0c51a0ccab24e7a100`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3066dd587e2e5fd44cc77bcf785a1eda6cb2c8fbfea705e112683712dc9bbf45`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de535d017baa9a7dbbcba70d7fde8cdb8607907fd1752fa99946ddf57958b2b0`  
		Last Modified: Thu, 15 Feb 2024 02:08:00 GMT  
		Size: 250.5 MB (250507125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1858c84143178e070fff903c762901603d1b1356e962f4fb73a71a200a55c84c`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:9a0e4ffc6087aabba7828052356da4cfbfb1db8f47eba6afec0c6bf93a96f3a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2322; amd64

### `julia:1.10.1-windowsservercore-ltsc2022` - windows version 10.0.20348.2322; amd64

```console
$ docker pull julia@sha256:ac7e7de1919e6a391278fd06062034d24dd1892f6569260439ea7a8aac745dd0
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2161166383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f26f77914b415046af8c139841e565707106b2048fc516c6c1cb8347d2a4f8`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Thu, 15 Feb 2024 01:55:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 15 Feb 2024 01:55:58 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 01:55:58 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.1-win64.exe
# Thu, 15 Feb 2024 01:55:59 GMT
ENV JULIA_SHA256=ca02e6bd4f771d51c72520f359d727679775c03f62e7e7e2595dd79d1d0e5fec
# Thu, 15 Feb 2024 01:57:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 15 Feb 2024 01:57:04 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ecd8f02f1b59d6f3aec1c570f2c8128d2b064a59e0da86653fdee442a472ad`  
		Last Modified: Thu, 15 Feb 2024 01:57:11 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62852f81701e842eaa34fb5baf41629e3a8bd717a09aeae6c9d8f85aa6d3d870`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a1387c2ad061bd6ecc5941ab04b037b84018b2bfddaa265150d148ffca73b4`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f3360ff5dce5375b4b898a4f4deb9f588e12659cb8db5611d7e3e01952b012`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44ebaee761d2302e12dcc0f6dc0d9e5debeb07658857a8749c1f96a07fa3bfb`  
		Last Modified: Thu, 15 Feb 2024 01:58:16 GMT  
		Size: 250.5 MB (250505768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c23a6fdc0fc3d51f4f3676cdf3a438f7d52cb9f9a6a964c4645f304cf900ff`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6`

```console
$ docker pull julia@sha256:a8327fa571294f5a20f999d4eb4cf859ffee5aedcd1af63075f02c88a74451fc
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
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

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
$ docker pull julia@sha256:cd18bc9c05e5990361b17223f251042c5ea80bb5db3b344cf195c792d99136f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143013539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f2470578923ebe27c671a0221b5d7bad8eeaec15579f6df3383cdc283f9ea5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 10 Nov 2023 15:26:46 GMT
ADD file:9766a0d12bded41ae2e7bcaa8d246afb6f5d5b6d2222e97193d07737d3f5b609 in / 
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
	-	`sha256:7a5e2a926145215a27b5a8051ed294061243135af64539be80d4449e05f71f52`  
		Last Modified: Tue, 13 Feb 2024 01:26:50 GMT  
		Size: 24.7 MB (24716645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceae075f3450a7e9c50ae3580cb72f75df9fc47d07296ab9654d02ef530559cf`  
		Last Modified: Thu, 15 Feb 2024 01:25:06 GMT  
		Size: 4.8 MB (4823646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b28f543e6efb4df82a81250388336cbfc1ba749cc7df24f263c79fb22074eca`  
		Last Modified: Thu, 15 Feb 2024 01:25:09 GMT  
		Size: 113.5 MB (113472881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f84b9f448a6149d0646f0c1f0fda6615f5f1900be4433b25ba2b9c5006da3a`  
		Last Modified: Thu, 15 Feb 2024 01:25:06 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.6` - unknown; unknown

```console
$ docker pull julia@sha256:af0584345df422b04495d56d1627a449894deed4dbf9602e260e2102aa20353e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f4988fc331cbdf733ec898642929a204f153330b9790f6f636815f3b89c0a4`

```dockerfile
```

-	Layers:
	-	`sha256:2c37b098f69c1b8023865b67f52d755a5b801fbe0e6f466ed2ebb5e82540f599`  
		Last Modified: Thu, 15 Feb 2024 01:25:06 GMT  
		Size: 2.1 MB (2117836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7d75ff6f26c9e20af0261d7ab2531f15bca589197af7290c9c45cba6153d613`  
		Last Modified: Thu, 15 Feb 2024 01:25:06 GMT  
		Size: 18.0 KB (18036 bytes)  
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

### `julia:1.6` - windows version 10.0.20348.2322; amd64

```console
$ docker pull julia@sha256:f06a3be786a46de736c3e26212b04d1adc2c9f9129f9cdb9637b4ce619a9afd9
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2045221096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a889647ca875a40b41e84884566e444695cf0a8b0e46f627dce184741db380bf`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Wed, 14 Feb 2024 20:02:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 20:02:04 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 14 Feb 2024 20:02:05 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Wed, 14 Feb 2024 20:02:06 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Wed, 14 Feb 2024 20:03:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Feb 2024 20:03:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457490b8e473b2b4cace85f16a053f806338c0f7f6a3bdff218ef433aa8d9925`  
		Last Modified: Wed, 14 Feb 2024 20:03:15 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1330800079b1af302ec1392d500f5310303e18c7aaab5901c572ca386ab32f9e`  
		Last Modified: Wed, 14 Feb 2024 20:03:13 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e2e48b5dfab73391db687a6f2066c15b350c21eb8b06975d02b5506fcbb8823`  
		Last Modified: Wed, 14 Feb 2024 20:03:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bbea6a91c85467b5dc010b854bd51f3c2d603d791cd85acda31cb0630956531`  
		Last Modified: Wed, 14 Feb 2024 20:03:12 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2132934be37a821c160de05a9eea153c52edadb206bf171b733282618b7be7`  
		Last Modified: Wed, 14 Feb 2024 20:03:30 GMT  
		Size: 134.6 MB (134560473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ab54560fce7dc9cfa812aaff0d340a39c86d341348a0cd6cd2b4698c238d28a`  
		Last Modified: Wed, 14 Feb 2024 20:03:13 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6` - windows version 10.0.17763.5458; amd64

```console
$ docker pull julia@sha256:09c90ff8e4be0ca5e3d923e99048df8c32dd0db6d9974da8626156c7b974f266
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2214998428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03b6ee973bf11b254f26ef822474ddce6fae1672f293e3896961b80698e8b99b`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 19:59:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 19:59:21 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 14 Feb 2024 19:59:22 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Wed, 14 Feb 2024 19:59:23 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Wed, 14 Feb 2024 20:00:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Feb 2024 20:00:52 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e605e004f4cb755af1169383158b75bedb97f524563dddfe35e57925afe72f5f`  
		Last Modified: Wed, 14 Feb 2024 20:00:56 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170e96888548549e4d59ddcd39595bc7953a365f6212d2a6940e2718a4dde7ce`  
		Last Modified: Wed, 14 Feb 2024 20:00:55 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f9a56da73420628232b4a4f79ca7c333929b19615c82aabfa0b2d67844f9a4`  
		Last Modified: Wed, 14 Feb 2024 20:00:55 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90dc828317be7c06823e558946da925cee6277a51b9ed0fd1a8c6dbe46a85737`  
		Last Modified: Wed, 14 Feb 2024 20:00:55 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8340310714b65a664db15a25d43f76aee6af7b8d6c771afb5dea5529ae6aa5da`  
		Last Modified: Wed, 14 Feb 2024 20:01:13 GMT  
		Size: 134.5 MB (134543168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b300e8dc526a2137e925d2cfe9065f66175312edfc044245f727acbb6adbaa19`  
		Last Modified: Wed, 14 Feb 2024 20:00:55 GMT  
		Size: 1.3 KB (1294 bytes)  
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
$ docker pull julia@sha256:ae70ce47c84011d2fb051d56477378be1402290f95effd6edf9f3085a91ba0e4
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
$ docker pull julia@sha256:cd18bc9c05e5990361b17223f251042c5ea80bb5db3b344cf195c792d99136f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143013539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f2470578923ebe27c671a0221b5d7bad8eeaec15579f6df3383cdc283f9ea5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 10 Nov 2023 15:26:46 GMT
ADD file:9766a0d12bded41ae2e7bcaa8d246afb6f5d5b6d2222e97193d07737d3f5b609 in / 
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
	-	`sha256:7a5e2a926145215a27b5a8051ed294061243135af64539be80d4449e05f71f52`  
		Last Modified: Tue, 13 Feb 2024 01:26:50 GMT  
		Size: 24.7 MB (24716645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceae075f3450a7e9c50ae3580cb72f75df9fc47d07296ab9654d02ef530559cf`  
		Last Modified: Thu, 15 Feb 2024 01:25:06 GMT  
		Size: 4.8 MB (4823646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b28f543e6efb4df82a81250388336cbfc1ba749cc7df24f263c79fb22074eca`  
		Last Modified: Thu, 15 Feb 2024 01:25:09 GMT  
		Size: 113.5 MB (113472881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f84b9f448a6149d0646f0c1f0fda6615f5f1900be4433b25ba2b9c5006da3a`  
		Last Modified: Thu, 15 Feb 2024 01:25:06 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.6-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:af0584345df422b04495d56d1627a449894deed4dbf9602e260e2102aa20353e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f4988fc331cbdf733ec898642929a204f153330b9790f6f636815f3b89c0a4`

```dockerfile
```

-	Layers:
	-	`sha256:2c37b098f69c1b8023865b67f52d755a5b801fbe0e6f466ed2ebb5e82540f599`  
		Last Modified: Thu, 15 Feb 2024 01:25:06 GMT  
		Size: 2.1 MB (2117836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7d75ff6f26c9e20af0261d7ab2531f15bca589197af7290c9c45cba6153d613`  
		Last Modified: Thu, 15 Feb 2024 01:25:06 GMT  
		Size: 18.0 KB (18036 bytes)  
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
$ docker pull julia@sha256:9f29b4438b254f28d4e7c334aec6059802519e1af7c1917476494cdeab884f26
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
$ docker pull julia@sha256:2dcf94fce56b8fca173db71407e8f23b0b8ba591151dff0fff92ed551c31e254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142284321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66539ce6f1a214667e5041bc4d9bce70e11f228db1f8d9c37fd22a6a8d0daaf9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 10 Nov 2023 15:26:46 GMT
ADD file:8904abb8948cc1601202f5f3dd63ae52e3b980ac6acafff765b9424bfd5defef in / 
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
	-	`sha256:7c57dc7cd6a5cd2a6636e8cbb774969d6394ce3ef35cb0d229f5cfbcd8ada61a`  
		Last Modified: Tue, 13 Feb 2024 01:27:40 GMT  
		Size: 26.6 MB (26582672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34de979132051e2799f8d805a8194d8f8d2b80709a8659d64ed9d495800ea8f8`  
		Last Modified: Thu, 15 Feb 2024 01:26:15 GMT  
		Size: 2.2 MB (2229196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503dff77092f1c220c529e6bbc7470211ba8857cdb95c93fa78f89b615ea586d`  
		Last Modified: Thu, 15 Feb 2024 01:26:18 GMT  
		Size: 113.5 MB (113472083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90514ff7c8f54e1908cfaac9a638527c044e62c484207335b4ed68c7bd38211e`  
		Last Modified: Thu, 15 Feb 2024 01:26:14 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.6-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:df53713b2ad289b3250f97b5ebd6a2894f3b284dc296707ed01cff694e16794a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2356332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1445f27ca7e7a02609d66f737e46983cd5be9af5cfdfe51d842e8707d0083073`

```dockerfile
```

-	Layers:
	-	`sha256:8760eceb37a69b0ad6b93eca10a475972570f5229776b6b8e34313a8cf4c0b94`  
		Last Modified: Thu, 15 Feb 2024 01:26:15 GMT  
		Size: 2.3 MB (2338896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:187cd9ec29342ba67a0aecadc34307a6bc513c1b4e87001cb656d1bd2f09a342`  
		Last Modified: Thu, 15 Feb 2024 01:26:15 GMT  
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
$ docker pull julia@sha256:abcfd3c42845d3e0616182ba52a7c39cba95636ea51e2aac716167db1e1151ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

### `julia:1.6-windowsservercore` - windows version 10.0.20348.2322; amd64

```console
$ docker pull julia@sha256:f06a3be786a46de736c3e26212b04d1adc2c9f9129f9cdb9637b4ce619a9afd9
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2045221096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a889647ca875a40b41e84884566e444695cf0a8b0e46f627dce184741db380bf`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Wed, 14 Feb 2024 20:02:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 20:02:04 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 14 Feb 2024 20:02:05 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Wed, 14 Feb 2024 20:02:06 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Wed, 14 Feb 2024 20:03:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Feb 2024 20:03:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457490b8e473b2b4cace85f16a053f806338c0f7f6a3bdff218ef433aa8d9925`  
		Last Modified: Wed, 14 Feb 2024 20:03:15 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1330800079b1af302ec1392d500f5310303e18c7aaab5901c572ca386ab32f9e`  
		Last Modified: Wed, 14 Feb 2024 20:03:13 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e2e48b5dfab73391db687a6f2066c15b350c21eb8b06975d02b5506fcbb8823`  
		Last Modified: Wed, 14 Feb 2024 20:03:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bbea6a91c85467b5dc010b854bd51f3c2d603d791cd85acda31cb0630956531`  
		Last Modified: Wed, 14 Feb 2024 20:03:12 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2132934be37a821c160de05a9eea153c52edadb206bf171b733282618b7be7`  
		Last Modified: Wed, 14 Feb 2024 20:03:30 GMT  
		Size: 134.6 MB (134560473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ab54560fce7dc9cfa812aaff0d340a39c86d341348a0cd6cd2b4698c238d28a`  
		Last Modified: Wed, 14 Feb 2024 20:03:13 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6-windowsservercore` - windows version 10.0.17763.5458; amd64

```console
$ docker pull julia@sha256:09c90ff8e4be0ca5e3d923e99048df8c32dd0db6d9974da8626156c7b974f266
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2214998428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03b6ee973bf11b254f26ef822474ddce6fae1672f293e3896961b80698e8b99b`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 19:59:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 19:59:21 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 14 Feb 2024 19:59:22 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Wed, 14 Feb 2024 19:59:23 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Wed, 14 Feb 2024 20:00:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Feb 2024 20:00:52 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e605e004f4cb755af1169383158b75bedb97f524563dddfe35e57925afe72f5f`  
		Last Modified: Wed, 14 Feb 2024 20:00:56 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170e96888548549e4d59ddcd39595bc7953a365f6212d2a6940e2718a4dde7ce`  
		Last Modified: Wed, 14 Feb 2024 20:00:55 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f9a56da73420628232b4a4f79ca7c333929b19615c82aabfa0b2d67844f9a4`  
		Last Modified: Wed, 14 Feb 2024 20:00:55 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90dc828317be7c06823e558946da925cee6277a51b9ed0fd1a8c6dbe46a85737`  
		Last Modified: Wed, 14 Feb 2024 20:00:55 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8340310714b65a664db15a25d43f76aee6af7b8d6c771afb5dea5529ae6aa5da`  
		Last Modified: Wed, 14 Feb 2024 20:01:13 GMT  
		Size: 134.5 MB (134543168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b300e8dc526a2137e925d2cfe9065f66175312edfc044245f727acbb6adbaa19`  
		Last Modified: Wed, 14 Feb 2024 20:00:55 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6-windowsservercore-1809`

```console
$ docker pull julia@sha256:c97329808ca9d3305dd0edbd110656217d217f430008cb73b39eb0c158ed32e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `julia:1.6-windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull julia@sha256:09c90ff8e4be0ca5e3d923e99048df8c32dd0db6d9974da8626156c7b974f266
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2214998428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03b6ee973bf11b254f26ef822474ddce6fae1672f293e3896961b80698e8b99b`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 19:59:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 19:59:21 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 14 Feb 2024 19:59:22 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Wed, 14 Feb 2024 19:59:23 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Wed, 14 Feb 2024 20:00:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Feb 2024 20:00:52 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e605e004f4cb755af1169383158b75bedb97f524563dddfe35e57925afe72f5f`  
		Last Modified: Wed, 14 Feb 2024 20:00:56 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170e96888548549e4d59ddcd39595bc7953a365f6212d2a6940e2718a4dde7ce`  
		Last Modified: Wed, 14 Feb 2024 20:00:55 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f9a56da73420628232b4a4f79ca7c333929b19615c82aabfa0b2d67844f9a4`  
		Last Modified: Wed, 14 Feb 2024 20:00:55 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90dc828317be7c06823e558946da925cee6277a51b9ed0fd1a8c6dbe46a85737`  
		Last Modified: Wed, 14 Feb 2024 20:00:55 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8340310714b65a664db15a25d43f76aee6af7b8d6c771afb5dea5529ae6aa5da`  
		Last Modified: Wed, 14 Feb 2024 20:01:13 GMT  
		Size: 134.5 MB (134543168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b300e8dc526a2137e925d2cfe9065f66175312edfc044245f727acbb6adbaa19`  
		Last Modified: Wed, 14 Feb 2024 20:00:55 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:54227ea243e8a34e82db0f7c083162a926d19bcf2e8fde8ab7487ffb9b170a3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2322; amd64

### `julia:1.6-windowsservercore-ltsc2022` - windows version 10.0.20348.2322; amd64

```console
$ docker pull julia@sha256:f06a3be786a46de736c3e26212b04d1adc2c9f9129f9cdb9637b4ce619a9afd9
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2045221096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a889647ca875a40b41e84884566e444695cf0a8b0e46f627dce184741db380bf`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Wed, 14 Feb 2024 20:02:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 20:02:04 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 14 Feb 2024 20:02:05 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Wed, 14 Feb 2024 20:02:06 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Wed, 14 Feb 2024 20:03:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Feb 2024 20:03:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457490b8e473b2b4cace85f16a053f806338c0f7f6a3bdff218ef433aa8d9925`  
		Last Modified: Wed, 14 Feb 2024 20:03:15 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1330800079b1af302ec1392d500f5310303e18c7aaab5901c572ca386ab32f9e`  
		Last Modified: Wed, 14 Feb 2024 20:03:13 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e2e48b5dfab73391db687a6f2066c15b350c21eb8b06975d02b5506fcbb8823`  
		Last Modified: Wed, 14 Feb 2024 20:03:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bbea6a91c85467b5dc010b854bd51f3c2d603d791cd85acda31cb0630956531`  
		Last Modified: Wed, 14 Feb 2024 20:03:12 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2132934be37a821c160de05a9eea153c52edadb206bf171b733282618b7be7`  
		Last Modified: Wed, 14 Feb 2024 20:03:30 GMT  
		Size: 134.6 MB (134560473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ab54560fce7dc9cfa812aaff0d340a39c86d341348a0cd6cd2b4698c238d28a`  
		Last Modified: Wed, 14 Feb 2024 20:03:13 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6.7`

```console
$ docker pull julia@sha256:a8327fa571294f5a20f999d4eb4cf859ffee5aedcd1af63075f02c88a74451fc
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
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

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
$ docker pull julia@sha256:cd18bc9c05e5990361b17223f251042c5ea80bb5db3b344cf195c792d99136f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143013539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f2470578923ebe27c671a0221b5d7bad8eeaec15579f6df3383cdc283f9ea5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 10 Nov 2023 15:26:46 GMT
ADD file:9766a0d12bded41ae2e7bcaa8d246afb6f5d5b6d2222e97193d07737d3f5b609 in / 
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
	-	`sha256:7a5e2a926145215a27b5a8051ed294061243135af64539be80d4449e05f71f52`  
		Last Modified: Tue, 13 Feb 2024 01:26:50 GMT  
		Size: 24.7 MB (24716645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceae075f3450a7e9c50ae3580cb72f75df9fc47d07296ab9654d02ef530559cf`  
		Last Modified: Thu, 15 Feb 2024 01:25:06 GMT  
		Size: 4.8 MB (4823646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b28f543e6efb4df82a81250388336cbfc1ba749cc7df24f263c79fb22074eca`  
		Last Modified: Thu, 15 Feb 2024 01:25:09 GMT  
		Size: 113.5 MB (113472881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f84b9f448a6149d0646f0c1f0fda6615f5f1900be4433b25ba2b9c5006da3a`  
		Last Modified: Thu, 15 Feb 2024 01:25:06 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.6.7` - unknown; unknown

```console
$ docker pull julia@sha256:af0584345df422b04495d56d1627a449894deed4dbf9602e260e2102aa20353e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f4988fc331cbdf733ec898642929a204f153330b9790f6f636815f3b89c0a4`

```dockerfile
```

-	Layers:
	-	`sha256:2c37b098f69c1b8023865b67f52d755a5b801fbe0e6f466ed2ebb5e82540f599`  
		Last Modified: Thu, 15 Feb 2024 01:25:06 GMT  
		Size: 2.1 MB (2117836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7d75ff6f26c9e20af0261d7ab2531f15bca589197af7290c9c45cba6153d613`  
		Last Modified: Thu, 15 Feb 2024 01:25:06 GMT  
		Size: 18.0 KB (18036 bytes)  
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

### `julia:1.6.7` - windows version 10.0.20348.2322; amd64

```console
$ docker pull julia@sha256:f06a3be786a46de736c3e26212b04d1adc2c9f9129f9cdb9637b4ce619a9afd9
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2045221096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a889647ca875a40b41e84884566e444695cf0a8b0e46f627dce184741db380bf`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Wed, 14 Feb 2024 20:02:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 20:02:04 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 14 Feb 2024 20:02:05 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Wed, 14 Feb 2024 20:02:06 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Wed, 14 Feb 2024 20:03:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Feb 2024 20:03:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457490b8e473b2b4cace85f16a053f806338c0f7f6a3bdff218ef433aa8d9925`  
		Last Modified: Wed, 14 Feb 2024 20:03:15 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1330800079b1af302ec1392d500f5310303e18c7aaab5901c572ca386ab32f9e`  
		Last Modified: Wed, 14 Feb 2024 20:03:13 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e2e48b5dfab73391db687a6f2066c15b350c21eb8b06975d02b5506fcbb8823`  
		Last Modified: Wed, 14 Feb 2024 20:03:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bbea6a91c85467b5dc010b854bd51f3c2d603d791cd85acda31cb0630956531`  
		Last Modified: Wed, 14 Feb 2024 20:03:12 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2132934be37a821c160de05a9eea153c52edadb206bf171b733282618b7be7`  
		Last Modified: Wed, 14 Feb 2024 20:03:30 GMT  
		Size: 134.6 MB (134560473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ab54560fce7dc9cfa812aaff0d340a39c86d341348a0cd6cd2b4698c238d28a`  
		Last Modified: Wed, 14 Feb 2024 20:03:13 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6.7` - windows version 10.0.17763.5458; amd64

```console
$ docker pull julia@sha256:09c90ff8e4be0ca5e3d923e99048df8c32dd0db6d9974da8626156c7b974f266
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2214998428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03b6ee973bf11b254f26ef822474ddce6fae1672f293e3896961b80698e8b99b`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 19:59:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 19:59:21 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 14 Feb 2024 19:59:22 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Wed, 14 Feb 2024 19:59:23 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Wed, 14 Feb 2024 20:00:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Feb 2024 20:00:52 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e605e004f4cb755af1169383158b75bedb97f524563dddfe35e57925afe72f5f`  
		Last Modified: Wed, 14 Feb 2024 20:00:56 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170e96888548549e4d59ddcd39595bc7953a365f6212d2a6940e2718a4dde7ce`  
		Last Modified: Wed, 14 Feb 2024 20:00:55 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f9a56da73420628232b4a4f79ca7c333929b19615c82aabfa0b2d67844f9a4`  
		Last Modified: Wed, 14 Feb 2024 20:00:55 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90dc828317be7c06823e558946da925cee6277a51b9ed0fd1a8c6dbe46a85737`  
		Last Modified: Wed, 14 Feb 2024 20:00:55 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8340310714b65a664db15a25d43f76aee6af7b8d6c771afb5dea5529ae6aa5da`  
		Last Modified: Wed, 14 Feb 2024 20:01:13 GMT  
		Size: 134.5 MB (134543168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b300e8dc526a2137e925d2cfe9065f66175312edfc044245f727acbb6adbaa19`  
		Last Modified: Wed, 14 Feb 2024 20:00:55 GMT  
		Size: 1.3 KB (1294 bytes)  
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
$ docker pull julia@sha256:ae70ce47c84011d2fb051d56477378be1402290f95effd6edf9f3085a91ba0e4
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
$ docker pull julia@sha256:cd18bc9c05e5990361b17223f251042c5ea80bb5db3b344cf195c792d99136f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143013539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f2470578923ebe27c671a0221b5d7bad8eeaec15579f6df3383cdc283f9ea5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 10 Nov 2023 15:26:46 GMT
ADD file:9766a0d12bded41ae2e7bcaa8d246afb6f5d5b6d2222e97193d07737d3f5b609 in / 
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
	-	`sha256:7a5e2a926145215a27b5a8051ed294061243135af64539be80d4449e05f71f52`  
		Last Modified: Tue, 13 Feb 2024 01:26:50 GMT  
		Size: 24.7 MB (24716645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceae075f3450a7e9c50ae3580cb72f75df9fc47d07296ab9654d02ef530559cf`  
		Last Modified: Thu, 15 Feb 2024 01:25:06 GMT  
		Size: 4.8 MB (4823646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b28f543e6efb4df82a81250388336cbfc1ba749cc7df24f263c79fb22074eca`  
		Last Modified: Thu, 15 Feb 2024 01:25:09 GMT  
		Size: 113.5 MB (113472881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f84b9f448a6149d0646f0c1f0fda6615f5f1900be4433b25ba2b9c5006da3a`  
		Last Modified: Thu, 15 Feb 2024 01:25:06 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.6.7-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:af0584345df422b04495d56d1627a449894deed4dbf9602e260e2102aa20353e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f4988fc331cbdf733ec898642929a204f153330b9790f6f636815f3b89c0a4`

```dockerfile
```

-	Layers:
	-	`sha256:2c37b098f69c1b8023865b67f52d755a5b801fbe0e6f466ed2ebb5e82540f599`  
		Last Modified: Thu, 15 Feb 2024 01:25:06 GMT  
		Size: 2.1 MB (2117836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7d75ff6f26c9e20af0261d7ab2531f15bca589197af7290c9c45cba6153d613`  
		Last Modified: Thu, 15 Feb 2024 01:25:06 GMT  
		Size: 18.0 KB (18036 bytes)  
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
$ docker pull julia@sha256:9f29b4438b254f28d4e7c334aec6059802519e1af7c1917476494cdeab884f26
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
$ docker pull julia@sha256:2dcf94fce56b8fca173db71407e8f23b0b8ba591151dff0fff92ed551c31e254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142284321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66539ce6f1a214667e5041bc4d9bce70e11f228db1f8d9c37fd22a6a8d0daaf9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 10 Nov 2023 15:26:46 GMT
ADD file:8904abb8948cc1601202f5f3dd63ae52e3b980ac6acafff765b9424bfd5defef in / 
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
	-	`sha256:7c57dc7cd6a5cd2a6636e8cbb774969d6394ce3ef35cb0d229f5cfbcd8ada61a`  
		Last Modified: Tue, 13 Feb 2024 01:27:40 GMT  
		Size: 26.6 MB (26582672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34de979132051e2799f8d805a8194d8f8d2b80709a8659d64ed9d495800ea8f8`  
		Last Modified: Thu, 15 Feb 2024 01:26:15 GMT  
		Size: 2.2 MB (2229196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503dff77092f1c220c529e6bbc7470211ba8857cdb95c93fa78f89b615ea586d`  
		Last Modified: Thu, 15 Feb 2024 01:26:18 GMT  
		Size: 113.5 MB (113472083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90514ff7c8f54e1908cfaac9a638527c044e62c484207335b4ed68c7bd38211e`  
		Last Modified: Thu, 15 Feb 2024 01:26:14 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.6.7-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:df53713b2ad289b3250f97b5ebd6a2894f3b284dc296707ed01cff694e16794a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2356332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1445f27ca7e7a02609d66f737e46983cd5be9af5cfdfe51d842e8707d0083073`

```dockerfile
```

-	Layers:
	-	`sha256:8760eceb37a69b0ad6b93eca10a475972570f5229776b6b8e34313a8cf4c0b94`  
		Last Modified: Thu, 15 Feb 2024 01:26:15 GMT  
		Size: 2.3 MB (2338896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:187cd9ec29342ba67a0aecadc34307a6bc513c1b4e87001cb656d1bd2f09a342`  
		Last Modified: Thu, 15 Feb 2024 01:26:15 GMT  
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
$ docker pull julia@sha256:abcfd3c42845d3e0616182ba52a7c39cba95636ea51e2aac716167db1e1151ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

### `julia:1.6.7-windowsservercore` - windows version 10.0.20348.2322; amd64

```console
$ docker pull julia@sha256:f06a3be786a46de736c3e26212b04d1adc2c9f9129f9cdb9637b4ce619a9afd9
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2045221096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a889647ca875a40b41e84884566e444695cf0a8b0e46f627dce184741db380bf`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Wed, 14 Feb 2024 20:02:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 20:02:04 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 14 Feb 2024 20:02:05 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Wed, 14 Feb 2024 20:02:06 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Wed, 14 Feb 2024 20:03:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Feb 2024 20:03:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457490b8e473b2b4cace85f16a053f806338c0f7f6a3bdff218ef433aa8d9925`  
		Last Modified: Wed, 14 Feb 2024 20:03:15 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1330800079b1af302ec1392d500f5310303e18c7aaab5901c572ca386ab32f9e`  
		Last Modified: Wed, 14 Feb 2024 20:03:13 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e2e48b5dfab73391db687a6f2066c15b350c21eb8b06975d02b5506fcbb8823`  
		Last Modified: Wed, 14 Feb 2024 20:03:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bbea6a91c85467b5dc010b854bd51f3c2d603d791cd85acda31cb0630956531`  
		Last Modified: Wed, 14 Feb 2024 20:03:12 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2132934be37a821c160de05a9eea153c52edadb206bf171b733282618b7be7`  
		Last Modified: Wed, 14 Feb 2024 20:03:30 GMT  
		Size: 134.6 MB (134560473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ab54560fce7dc9cfa812aaff0d340a39c86d341348a0cd6cd2b4698c238d28a`  
		Last Modified: Wed, 14 Feb 2024 20:03:13 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6.7-windowsservercore` - windows version 10.0.17763.5458; amd64

```console
$ docker pull julia@sha256:09c90ff8e4be0ca5e3d923e99048df8c32dd0db6d9974da8626156c7b974f266
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2214998428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03b6ee973bf11b254f26ef822474ddce6fae1672f293e3896961b80698e8b99b`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 19:59:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 19:59:21 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 14 Feb 2024 19:59:22 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Wed, 14 Feb 2024 19:59:23 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Wed, 14 Feb 2024 20:00:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Feb 2024 20:00:52 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e605e004f4cb755af1169383158b75bedb97f524563dddfe35e57925afe72f5f`  
		Last Modified: Wed, 14 Feb 2024 20:00:56 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170e96888548549e4d59ddcd39595bc7953a365f6212d2a6940e2718a4dde7ce`  
		Last Modified: Wed, 14 Feb 2024 20:00:55 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f9a56da73420628232b4a4f79ca7c333929b19615c82aabfa0b2d67844f9a4`  
		Last Modified: Wed, 14 Feb 2024 20:00:55 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90dc828317be7c06823e558946da925cee6277a51b9ed0fd1a8c6dbe46a85737`  
		Last Modified: Wed, 14 Feb 2024 20:00:55 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8340310714b65a664db15a25d43f76aee6af7b8d6c771afb5dea5529ae6aa5da`  
		Last Modified: Wed, 14 Feb 2024 20:01:13 GMT  
		Size: 134.5 MB (134543168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b300e8dc526a2137e925d2cfe9065f66175312edfc044245f727acbb6adbaa19`  
		Last Modified: Wed, 14 Feb 2024 20:00:55 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6.7-windowsservercore-1809`

```console
$ docker pull julia@sha256:c97329808ca9d3305dd0edbd110656217d217f430008cb73b39eb0c158ed32e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `julia:1.6.7-windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull julia@sha256:09c90ff8e4be0ca5e3d923e99048df8c32dd0db6d9974da8626156c7b974f266
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2214998428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03b6ee973bf11b254f26ef822474ddce6fae1672f293e3896961b80698e8b99b`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 19:59:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 19:59:21 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 14 Feb 2024 19:59:22 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Wed, 14 Feb 2024 19:59:23 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Wed, 14 Feb 2024 20:00:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Feb 2024 20:00:52 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e605e004f4cb755af1169383158b75bedb97f524563dddfe35e57925afe72f5f`  
		Last Modified: Wed, 14 Feb 2024 20:00:56 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170e96888548549e4d59ddcd39595bc7953a365f6212d2a6940e2718a4dde7ce`  
		Last Modified: Wed, 14 Feb 2024 20:00:55 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f9a56da73420628232b4a4f79ca7c333929b19615c82aabfa0b2d67844f9a4`  
		Last Modified: Wed, 14 Feb 2024 20:00:55 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90dc828317be7c06823e558946da925cee6277a51b9ed0fd1a8c6dbe46a85737`  
		Last Modified: Wed, 14 Feb 2024 20:00:55 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8340310714b65a664db15a25d43f76aee6af7b8d6c771afb5dea5529ae6aa5da`  
		Last Modified: Wed, 14 Feb 2024 20:01:13 GMT  
		Size: 134.5 MB (134543168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b300e8dc526a2137e925d2cfe9065f66175312edfc044245f727acbb6adbaa19`  
		Last Modified: Wed, 14 Feb 2024 20:00:55 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6.7-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:54227ea243e8a34e82db0f7c083162a926d19bcf2e8fde8ab7487ffb9b170a3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2322; amd64

### `julia:1.6.7-windowsservercore-ltsc2022` - windows version 10.0.20348.2322; amd64

```console
$ docker pull julia@sha256:f06a3be786a46de736c3e26212b04d1adc2c9f9129f9cdb9637b4ce619a9afd9
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2045221096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a889647ca875a40b41e84884566e444695cf0a8b0e46f627dce184741db380bf`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Wed, 14 Feb 2024 20:02:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 20:02:04 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 14 Feb 2024 20:02:05 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Wed, 14 Feb 2024 20:02:06 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Wed, 14 Feb 2024 20:03:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Feb 2024 20:03:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457490b8e473b2b4cace85f16a053f806338c0f7f6a3bdff218ef433aa8d9925`  
		Last Modified: Wed, 14 Feb 2024 20:03:15 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1330800079b1af302ec1392d500f5310303e18c7aaab5901c572ca386ab32f9e`  
		Last Modified: Wed, 14 Feb 2024 20:03:13 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e2e48b5dfab73391db687a6f2066c15b350c21eb8b06975d02b5506fcbb8823`  
		Last Modified: Wed, 14 Feb 2024 20:03:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bbea6a91c85467b5dc010b854bd51f3c2d603d791cd85acda31cb0630956531`  
		Last Modified: Wed, 14 Feb 2024 20:03:12 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2132934be37a821c160de05a9eea153c52edadb206bf171b733282618b7be7`  
		Last Modified: Wed, 14 Feb 2024 20:03:30 GMT  
		Size: 134.6 MB (134560473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ab54560fce7dc9cfa812aaff0d340a39c86d341348a0cd6cd2b4698c238d28a`  
		Last Modified: Wed, 14 Feb 2024 20:03:13 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:alpine`

```console
$ docker pull julia@sha256:38e9661d58c48669b03a2b9be0bb4c4fb995f270442388854bab380043c41e2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:alpine` - linux; amd64

```console
$ docker pull julia@sha256:da0ebe0fdd8d2973c4cbe6c0b441739707a9173f47bf641dc5a0ded3e2d8ad4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.6 MB (177599522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4629a432942eac3a84338692a5217c4758a13da1e447a17b943a4ee5d0cf6357`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.1-musl-x86_64.tar.gz'; 			sha256='48e643c431f156e0cec440e3881f09dd78491c59de7804c73f470fba8cd64d1d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68eaf8cd85ce8bc2f83dd044858e77dc6ea04d797dcee4d4619f3a1dde5f73f1`  
		Last Modified: Thu, 15 Feb 2024 01:52:38 GMT  
		Size: 174.2 MB (174190425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e61b9b3f6995be6208e105dc44d9228d5bc22dc0570c34dbc7dfdd0dfb21b9e`  
		Last Modified: Thu, 15 Feb 2024 01:52:36 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:alpine` - unknown; unknown

```console
$ docker pull julia@sha256:07ab0484248a0b54bc9ccb67a15926fee6ecc1962552ddb0fc93651894af2a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.5 KB (119496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd5b516084ce3e9b080769c76191451657aab08f6d5bebe3ef5668280c39380`

```dockerfile
```

-	Layers:
	-	`sha256:ecaca48c94c6b70ef43edb0d3450d5d2d4cf2a5f5f18ef3b14326697c0a7c529`  
		Last Modified: Thu, 15 Feb 2024 01:52:36 GMT  
		Size: 104.8 KB (104799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bba9bd77ce2c5fd4ab756f06d5010801f772e290016bf8c6a1fc066d5c37d42`  
		Last Modified: Thu, 15 Feb 2024 01:52:36 GMT  
		Size: 14.7 KB (14697 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:alpine3.18`

```console
$ docker pull julia@sha256:4ec8fa66b1b062c5c7d0ce6c0796ba0c4ea4e5df6cfc03e43e30167e3eb30ad2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:alpine3.18` - linux; amd64

```console
$ docker pull julia@sha256:e2e9526bf3bab718c84a9929115093953198eb43106374f04f9820f47c25997e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.6 MB (177593364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba54d9793c9d669939bcee642131032584105a0feaad52c06e388cf0d9e219b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.1-musl-x86_64.tar.gz'; 			sha256='48e643c431f156e0cec440e3881f09dd78491c59de7804c73f470fba8cd64d1d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=alpine&os_version=3.18"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef7909ee5233603cda10c2ca32601363045f0197c5f7ce5a3ab10251331176b`  
		Last Modified: Thu, 15 Feb 2024 01:52:50 GMT  
		Size: 174.2 MB (174190453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815110e9a9cb295a7eda0be2b78d3ce7016aa3a82d3d1b7791caf3bc003d9324`  
		Last Modified: Thu, 15 Feb 2024 01:52:47 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:alpine3.18` - unknown; unknown

```console
$ docker pull julia@sha256:7ae9f8f1ea5c2931c587ba63d2a8767bd35581eaf529e7390360469a88ec3434
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.5 KB (116519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df13cc1780fc7df1654365138f14d5147b21018d3a1d5f7238a0ac203b04b87e`

```dockerfile
```

-	Layers:
	-	`sha256:6fd0845ed3571a63743ec9da097c8e95cd1eb993e6cc66e605d7aaf438f3675a`  
		Last Modified: Thu, 15 Feb 2024 01:52:47 GMT  
		Size: 103.0 KB (103033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1393768754e0e0cd1f9f537f6a992341f9030f04e0e05217179713c8e4a0e4f`  
		Last Modified: Thu, 15 Feb 2024 01:52:47 GMT  
		Size: 13.5 KB (13486 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:alpine3.19`

```console
$ docker pull julia@sha256:38e9661d58c48669b03a2b9be0bb4c4fb995f270442388854bab380043c41e2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:alpine3.19` - linux; amd64

```console
$ docker pull julia@sha256:da0ebe0fdd8d2973c4cbe6c0b441739707a9173f47bf641dc5a0ded3e2d8ad4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.6 MB (177599522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4629a432942eac3a84338692a5217c4758a13da1e447a17b943a4ee5d0cf6357`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.1-musl-x86_64.tar.gz'; 			sha256='48e643c431f156e0cec440e3881f09dd78491c59de7804c73f470fba8cd64d1d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68eaf8cd85ce8bc2f83dd044858e77dc6ea04d797dcee4d4619f3a1dde5f73f1`  
		Last Modified: Thu, 15 Feb 2024 01:52:38 GMT  
		Size: 174.2 MB (174190425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e61b9b3f6995be6208e105dc44d9228d5bc22dc0570c34dbc7dfdd0dfb21b9e`  
		Last Modified: Thu, 15 Feb 2024 01:52:36 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:alpine3.19` - unknown; unknown

```console
$ docker pull julia@sha256:07ab0484248a0b54bc9ccb67a15926fee6ecc1962552ddb0fc93651894af2a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.5 KB (119496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd5b516084ce3e9b080769c76191451657aab08f6d5bebe3ef5668280c39380`

```dockerfile
```

-	Layers:
	-	`sha256:ecaca48c94c6b70ef43edb0d3450d5d2d4cf2a5f5f18ef3b14326697c0a7c529`  
		Last Modified: Thu, 15 Feb 2024 01:52:36 GMT  
		Size: 104.8 KB (104799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bba9bd77ce2c5fd4ab756f06d5010801f772e290016bf8c6a1fc066d5c37d42`  
		Last Modified: Thu, 15 Feb 2024 01:52:36 GMT  
		Size: 14.7 KB (14697 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:bookworm`

```console
$ docker pull julia@sha256:687d51426b84545c07df8d8e90a6d40c8a9ecc6a4d1ec6143d3d8237a9d5d0dc
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
$ docker pull julia@sha256:3caf5e0e4797801b5afa0cdb559075e1f7226c7ea16a3153fe7d18769aba94e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.2 MB (205223283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae4a5eea63105374a0e3ad6f704dedf7bf406350ddb98b6ad13582428fa24df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.1-linux-x86_64.tar.gz'; 			sha256='fe924258e55d074410b134195cf6b85cbe8f307fcd05a4fdd23f8944c5941a70'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.1-linux-aarch64.tar.gz'; 			sha256='67e912a2b8ae0fd2469a1a42c7d70b18cdf30b06dc717653fac64b710ca0575e'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.1-linux-i686.tar.gz'; 			sha256='46ae06f5690b4812e091f8e2a1b8a1caf849b5c842e8c7c3b8e474aaa7302526'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b760910a8ea7efbbc01dd05c522c09fbb768992e3e65929cf016f8a28e719d7`  
		Last Modified: Thu, 15 Feb 2024 01:52:52 GMT  
		Size: 5.7 MB (5707930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd429a837e23f6998e27565211ae302823134f3abdcf89d5a7c9400204139c55`  
		Last Modified: Thu, 15 Feb 2024 01:52:56 GMT  
		Size: 170.4 MB (170390890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6284bd0c80ca3e758d54e5f4f5076c25ccebccbba5d1108ef3ba6bc1703e73`  
		Last Modified: Thu, 15 Feb 2024 01:52:52 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:758cf0885b58460ec61796007b01d32c41f514dc0e1f8447e9a99f881f6666dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2158113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13bb7fc6510c67ceb8c7e7b0e22270d2ab6c904c71fc91de34003938191ebee1`

```dockerfile
```

-	Layers:
	-	`sha256:fe238e30162271ec796cf27837b3f1d078051f6979b4a0231cba428ae6598966`  
		Last Modified: Thu, 15 Feb 2024 01:52:52 GMT  
		Size: 2.1 MB (2139403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59fbd28bbcc24b3f7bb1c4f252a545a1236ff7692d9643ab5983bf53d2ef990b`  
		Last Modified: Thu, 15 Feb 2024 01:52:51 GMT  
		Size: 18.7 KB (18710 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:c7899893acb41c45312f7bcdc32512504b58ede63f02a0bba4dca92a272dbfda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.7 MB (199690181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:953f39f3ca0da48a4a5caebe30cc5d44769e6b518af75d4b51ce1f2b85fd7eaa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
CMD ["bash"]
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.1-linux-x86_64.tar.gz'; 			sha256='fe924258e55d074410b134195cf6b85cbe8f307fcd05a4fdd23f8944c5941a70'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.1-linux-aarch64.tar.gz'; 			sha256='67e912a2b8ae0fd2469a1a42c7d70b18cdf30b06dc717653fac64b710ca0575e'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.1-linux-i686.tar.gz'; 			sha256='46ae06f5690b4812e091f8e2a1b8a1caf849b5c842e8c7c3b8e474aaa7302526'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
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
	-	`sha256:df0a7047eef5296003128d4756f1f1b85b64c3f77206da6c62d958fc9572f10a`  
		Last Modified: Thu, 15 Feb 2024 02:14:07 GMT  
		Size: 165.0 MB (165000301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9f16d4c44b43675a53f7695a26f28e3cc7b16e7e71b0dddd82233834973fb3`  
		Last Modified: Thu, 15 Feb 2024 02:14:03 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:aaee047bc50ce902be26894ad0f4f267dda17086bf85430a1159a7ca679533de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2157334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c644ea6ef587504b4b31a9b2946c85895ec0a36586b46679c63753215cc4b8cd`

```dockerfile
```

-	Layers:
	-	`sha256:6ef921af30be56f765d798735060cdf175b864621010058e5c33ad36ac7a00b9`  
		Last Modified: Thu, 15 Feb 2024 02:14:03 GMT  
		Size: 2.1 MB (2138773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6bbf6d09ba5d03bb45cd1ca38605efef1b6f6227352ec90c0d7041a312e1e03`  
		Last Modified: Thu, 15 Feb 2024 02:14:03 GMT  
		Size: 18.6 KB (18561 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; 386

```console
$ docker pull julia@sha256:c733805bb2115e3e7ac2293646a60c5c37145d14575ae13a887543f7cfcfb120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192500887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27155dea2c1a627acfc854ba5afb07edabdbf706f1d74a0df905d2af1d98ace`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:56 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Tue, 13 Feb 2024 00:38:56 GMT
CMD ["bash"]
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.1-linux-x86_64.tar.gz'; 			sha256='fe924258e55d074410b134195cf6b85cbe8f307fcd05a4fdd23f8944c5941a70'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.1-linux-aarch64.tar.gz'; 			sha256='67e912a2b8ae0fd2469a1a42c7d70b18cdf30b06dc717653fac64b710ca0575e'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.1-linux-i686.tar.gz'; 			sha256='46ae06f5690b4812e091f8e2a1b8a1caf849b5c842e8c7c3b8e474aaa7302526'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b060bee81687c0dd068e9e9bb305e7d29ed2e3599f2ad66b28f8b70956a9fd21`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 5.9 MB (5863219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0a9393e3d7ec1e1d267186dd2e07326e97b56b875a4bb284b88b54504d9121`  
		Last Modified: Thu, 15 Feb 2024 01:52:46 GMT  
		Size: 156.5 MB (156495490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28dd21637325ca9b78d6c7e0a451b94a842713f5d96b2dfe69077bd35f7b44f`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:1460d63336cc97e4810367a540f40251647c57e6c86390c26469cf7da2b54930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2155240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4e048bdbabc6b4032e5cab36750926cf4d48be404b13f1d86268c55af218916`

```dockerfile
```

-	Layers:
	-	`sha256:0c29468e89b817688be1fa9de743c5e24910501b2881091894d40e5e6a71c2cb`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 2.1 MB (2136581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdd8305c04fcac3daa8caffcbcc79c942a6871f59a617792ec7e5741cc95c75b`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 18.7 KB (18659 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:bullseye`

```console
$ docker pull julia@sha256:7ad8dfad6efa322a660d6dd97a4f51d593e5ca3af248a8a10b07536169c13d28
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
$ docker pull julia@sha256:24c742c0cc59e688cca2b4064189e37ed35878c7f1709a2cffa3c8d89d64ddc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.2 MB (204239761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a882b29e497eb3cbd9ee464ae98d65cf2af1741338cc88dd8761fada5fb008`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.1-linux-x86_64.tar.gz'; 			sha256='fe924258e55d074410b134195cf6b85cbe8f307fcd05a4fdd23f8944c5941a70'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.1-linux-aarch64.tar.gz'; 			sha256='67e912a2b8ae0fd2469a1a42c7d70b18cdf30b06dc717653fac64b710ca0575e'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.1-linux-i686.tar.gz'; 			sha256='46ae06f5690b4812e091f8e2a1b8a1caf849b5c842e8c7c3b8e474aaa7302526'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52994ac9c626986c541c9af48e43ce1e0640e1923e36e90f5d0fac837147ce4f`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 2.4 MB (2426548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2953fea1f932882e3271c8cb61836952f6f90cfbaa344e8986500308c0cfe350`  
		Last Modified: Thu, 15 Feb 2024 01:52:45 GMT  
		Size: 170.4 MB (170390420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ddfead841b8c9404e76dd94b0b7a2340f8535ae2519d8fadfd50f6910a3b50a`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:2d799f94368b3ce51d7c73df4f866409c4274bbdd86f24af6604befc903ff1a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f294f1fdee6ae56922f01b720082730221f68e19fb7128cd6b956ec44ef36124`

```dockerfile
```

-	Layers:
	-	`sha256:74f859ebca0253d35bc9e06a1902608fa6958f913875dd6c9c4332601900ef57`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 2.4 MB (2359909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b86568a9b88e5470630bc40bf42cf53d203c35ff5d496a57d2f38fc9565de2c`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 17.5 KB (17540 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:99a7a3642824f780c5063e3332f761b4254397660f29b86033ee0c76042d8c42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.5 MB (197487223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e371987ac33efcf3b92b1e37091a25ce5adf8792a55f6670ffdf9ae1217acb3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.1-linux-x86_64.tar.gz'; 			sha256='fe924258e55d074410b134195cf6b85cbe8f307fcd05a4fdd23f8944c5941a70'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.1-linux-aarch64.tar.gz'; 			sha256='67e912a2b8ae0fd2469a1a42c7d70b18cdf30b06dc717653fac64b710ca0575e'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.1-linux-i686.tar.gz'; 			sha256='46ae06f5690b4812e091f8e2a1b8a1caf849b5c842e8c7c3b8e474aaa7302526'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
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
	-	`sha256:4fdc35222d7fcab46d11964d7e268775a9e4dbeebda85291a301ed8e3f38f12d`  
		Last Modified: Thu, 15 Feb 2024 02:15:10 GMT  
		Size: 165.0 MB (165000735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad69da563be9c7b3dc8b611885665f62220ebe6398e81be8b290f77b0269b90`  
		Last Modified: Thu, 15 Feb 2024 02:15:07 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:b8ff89e6d9cbd111de03fc482476ae6906c3e816120f66197e3238d29dd1f98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2376644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0a75eebe54c1ec99e9c01002195b63a859a0886f69df77d25e26c0ea55014bd`

```dockerfile
```

-	Layers:
	-	`sha256:8dc77e10839b1fb9c0dec75843295adca36d084e87b48ada981a892c3778d312`  
		Last Modified: Thu, 15 Feb 2024 02:15:06 GMT  
		Size: 2.4 MB (2359261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18b6801e86d58f2bb78f3906b735cd5539178e9c21fcfaeea7db87c57d3d825b`  
		Last Modified: Thu, 15 Feb 2024 02:15:06 GMT  
		Size: 17.4 KB (17383 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bullseye` - linux; 386

```console
$ docker pull julia@sha256:4cc3e8cc1fc2445d3c8958223fb7ff3ed7386fcc59053b4fbb52caa0b8b135f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191436740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a89c723882a8e89f126a53b96a86330d39b04f7fd394adb5be01967629f4a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:18 GMT
ADD file:9eaee5af136d095dc1dac0ffce0fde09d8f1bd02ff7cb65ee67e00b2a66f34f7 in / 
# Tue, 13 Feb 2024 00:39:19 GMT
CMD ["bash"]
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.1-linux-x86_64.tar.gz'; 			sha256='fe924258e55d074410b134195cf6b85cbe8f307fcd05a4fdd23f8944c5941a70'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.1-linux-aarch64.tar.gz'; 			sha256='67e912a2b8ae0fd2469a1a42c7d70b18cdf30b06dc717653fac64b710ca0575e'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.1-linux-i686.tar.gz'; 			sha256='46ae06f5690b4812e091f8e2a1b8a1caf849b5c842e8c7c3b8e474aaa7302526'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1ac8173b08d16f9f136fb0e3ee39999cef7495f924ecb43f3ca4a4eea267cc88`  
		Last Modified: Tue, 13 Feb 2024 00:44:36 GMT  
		Size: 32.4 MB (32407443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c2a21aba0b258d2d59ed768ff41751fcc88255368a239a0c26c72579e241ac`  
		Last Modified: Thu, 15 Feb 2024 01:52:40 GMT  
		Size: 2.5 MB (2533021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d246a08907e76876dc75135451dddc888bc48ceee300a8336e3172f79d0d246`  
		Last Modified: Thu, 15 Feb 2024 01:52:44 GMT  
		Size: 156.5 MB (156495904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45acd41394aa2be9e84237ed4d84fb4b41efa03ffdae3fee7ffe23d93fcc587f`  
		Last Modified: Thu, 15 Feb 2024 01:52:40 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:f324c95527f73df472f020fe9ad52ca74da2c87ea065cfc19eecf21d5d5ee350
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2374624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da94324fe8ee54c3188af2712264ee35eb43fcfbd1ffcfaff78c507270b0b33`

```dockerfile
```

-	Layers:
	-	`sha256:cbf974f51c72a3dabef9dfde0558dc77052a511c4f7b23f57744ad1d82a71698`  
		Last Modified: Thu, 15 Feb 2024 01:52:40 GMT  
		Size: 2.4 MB (2357115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44c5e6153327499afffa4e26339c505637b4ed975cb6175112ad50d21df77e8d`  
		Last Modified: Thu, 15 Feb 2024 01:52:40 GMT  
		Size: 17.5 KB (17509 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:latest`

```console
$ docker pull julia@sha256:2d992bcdfd817a11bfa70918879674b62dcd0a497e079116605c33dc9979589e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

### `julia:latest` - linux; amd64

```console
$ docker pull julia@sha256:3caf5e0e4797801b5afa0cdb559075e1f7226c7ea16a3153fe7d18769aba94e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.2 MB (205223283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae4a5eea63105374a0e3ad6f704dedf7bf406350ddb98b6ad13582428fa24df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.1-linux-x86_64.tar.gz'; 			sha256='fe924258e55d074410b134195cf6b85cbe8f307fcd05a4fdd23f8944c5941a70'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.1-linux-aarch64.tar.gz'; 			sha256='67e912a2b8ae0fd2469a1a42c7d70b18cdf30b06dc717653fac64b710ca0575e'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.1-linux-i686.tar.gz'; 			sha256='46ae06f5690b4812e091f8e2a1b8a1caf849b5c842e8c7c3b8e474aaa7302526'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b760910a8ea7efbbc01dd05c522c09fbb768992e3e65929cf016f8a28e719d7`  
		Last Modified: Thu, 15 Feb 2024 01:52:52 GMT  
		Size: 5.7 MB (5707930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd429a837e23f6998e27565211ae302823134f3abdcf89d5a7c9400204139c55`  
		Last Modified: Thu, 15 Feb 2024 01:52:56 GMT  
		Size: 170.4 MB (170390890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6284bd0c80ca3e758d54e5f4f5076c25ccebccbba5d1108ef3ba6bc1703e73`  
		Last Modified: Thu, 15 Feb 2024 01:52:52 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:758cf0885b58460ec61796007b01d32c41f514dc0e1f8447e9a99f881f6666dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2158113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13bb7fc6510c67ceb8c7e7b0e22270d2ab6c904c71fc91de34003938191ebee1`

```dockerfile
```

-	Layers:
	-	`sha256:fe238e30162271ec796cf27837b3f1d078051f6979b4a0231cba428ae6598966`  
		Last Modified: Thu, 15 Feb 2024 01:52:52 GMT  
		Size: 2.1 MB (2139403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59fbd28bbcc24b3f7bb1c4f252a545a1236ff7692d9643ab5983bf53d2ef990b`  
		Last Modified: Thu, 15 Feb 2024 01:52:51 GMT  
		Size: 18.7 KB (18710 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:c7899893acb41c45312f7bcdc32512504b58ede63f02a0bba4dca92a272dbfda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.7 MB (199690181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:953f39f3ca0da48a4a5caebe30cc5d44769e6b518af75d4b51ce1f2b85fd7eaa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
CMD ["bash"]
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.1-linux-x86_64.tar.gz'; 			sha256='fe924258e55d074410b134195cf6b85cbe8f307fcd05a4fdd23f8944c5941a70'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.1-linux-aarch64.tar.gz'; 			sha256='67e912a2b8ae0fd2469a1a42c7d70b18cdf30b06dc717653fac64b710ca0575e'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.1-linux-i686.tar.gz'; 			sha256='46ae06f5690b4812e091f8e2a1b8a1caf849b5c842e8c7c3b8e474aaa7302526'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
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
	-	`sha256:df0a7047eef5296003128d4756f1f1b85b64c3f77206da6c62d958fc9572f10a`  
		Last Modified: Thu, 15 Feb 2024 02:14:07 GMT  
		Size: 165.0 MB (165000301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9f16d4c44b43675a53f7695a26f28e3cc7b16e7e71b0dddd82233834973fb3`  
		Last Modified: Thu, 15 Feb 2024 02:14:03 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:aaee047bc50ce902be26894ad0f4f267dda17086bf85430a1159a7ca679533de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2157334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c644ea6ef587504b4b31a9b2946c85895ec0a36586b46679c63753215cc4b8cd`

```dockerfile
```

-	Layers:
	-	`sha256:6ef921af30be56f765d798735060cdf175b864621010058e5c33ad36ac7a00b9`  
		Last Modified: Thu, 15 Feb 2024 02:14:03 GMT  
		Size: 2.1 MB (2138773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6bbf6d09ba5d03bb45cd1ca38605efef1b6f6227352ec90c0d7041a312e1e03`  
		Last Modified: Thu, 15 Feb 2024 02:14:03 GMT  
		Size: 18.6 KB (18561 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; 386

```console
$ docker pull julia@sha256:c733805bb2115e3e7ac2293646a60c5c37145d14575ae13a887543f7cfcfb120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192500887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27155dea2c1a627acfc854ba5afb07edabdbf706f1d74a0df905d2af1d98ace`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:56 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Tue, 13 Feb 2024 00:38:56 GMT
CMD ["bash"]
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Feb 2024 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 15 Feb 2024 00:59:15 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 00:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.1-linux-x86_64.tar.gz'; 			sha256='fe924258e55d074410b134195cf6b85cbe8f307fcd05a4fdd23f8944c5941a70'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.1-linux-aarch64.tar.gz'; 			sha256='67e912a2b8ae0fd2469a1a42c7d70b18cdf30b06dc717653fac64b710ca0575e'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.1-linux-i686.tar.gz'; 			sha256='46ae06f5690b4812e091f8e2a1b8a1caf849b5c842e8c7c3b8e474aaa7302526'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.1?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 00:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b060bee81687c0dd068e9e9bb305e7d29ed2e3599f2ad66b28f8b70956a9fd21`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 5.9 MB (5863219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0a9393e3d7ec1e1d267186dd2e07326e97b56b875a4bb284b88b54504d9121`  
		Last Modified: Thu, 15 Feb 2024 01:52:46 GMT  
		Size: 156.5 MB (156495490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28dd21637325ca9b78d6c7e0a451b94a842713f5d96b2dfe69077bd35f7b44f`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:1460d63336cc97e4810367a540f40251647c57e6c86390c26469cf7da2b54930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2155240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4e048bdbabc6b4032e5cab36750926cf4d48be404b13f1d86268c55af218916`

```dockerfile
```

-	Layers:
	-	`sha256:0c29468e89b817688be1fa9de743c5e24910501b2881091894d40e5e6a71c2cb`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 2.1 MB (2136581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdd8305c04fcac3daa8caffcbcc79c942a6871f59a617792ec7e5741cc95c75b`  
		Last Modified: Thu, 15 Feb 2024 01:52:42 GMT  
		Size: 18.7 KB (18659 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - windows version 10.0.20348.2322; amd64

```console
$ docker pull julia@sha256:ac7e7de1919e6a391278fd06062034d24dd1892f6569260439ea7a8aac745dd0
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2161166383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f26f77914b415046af8c139841e565707106b2048fc516c6c1cb8347d2a4f8`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Thu, 15 Feb 2024 01:55:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 15 Feb 2024 01:55:58 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 01:55:58 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.1-win64.exe
# Thu, 15 Feb 2024 01:55:59 GMT
ENV JULIA_SHA256=ca02e6bd4f771d51c72520f359d727679775c03f62e7e7e2595dd79d1d0e5fec
# Thu, 15 Feb 2024 01:57:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 15 Feb 2024 01:57:04 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ecd8f02f1b59d6f3aec1c570f2c8128d2b064a59e0da86653fdee442a472ad`  
		Last Modified: Thu, 15 Feb 2024 01:57:11 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62852f81701e842eaa34fb5baf41629e3a8bd717a09aeae6c9d8f85aa6d3d870`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a1387c2ad061bd6ecc5941ab04b037b84018b2bfddaa265150d148ffca73b4`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f3360ff5dce5375b4b898a4f4deb9f588e12659cb8db5611d7e3e01952b012`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44ebaee761d2302e12dcc0f6dc0d9e5debeb07658857a8749c1f96a07fa3bfb`  
		Last Modified: Thu, 15 Feb 2024 01:58:16 GMT  
		Size: 250.5 MB (250505768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c23a6fdc0fc3d51f4f3676cdf3a438f7d52cb9f9a6a964c4645f304cf900ff`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.17763.5458; amd64

```console
$ docker pull julia@sha256:0955c5756b87875173c9a5b65b2df8cbb7d5b390c9c4550f7f521c40b3fa1935
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2330962381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef0a0692cd89c0ebd705bcc2f6c2ddf0fa8c2f800111fbf1041ec324ce62832a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Thu, 15 Feb 2024 02:05:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 15 Feb 2024 02:05:41 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 02:05:42 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.1-win64.exe
# Thu, 15 Feb 2024 02:05:43 GMT
ENV JULIA_SHA256=ca02e6bd4f771d51c72520f359d727679775c03f62e7e7e2595dd79d1d0e5fec
# Thu, 15 Feb 2024 02:07:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 15 Feb 2024 02:07:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ed3e36144d60ff8117a3dd6eb64daa4e29953bb129aaad397b30092f9cc4c1`  
		Last Modified: Thu, 15 Feb 2024 02:07:25 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ff9d169a5e63801023c2b6a0a537977e5c7505d96e3c8896d7dfeadf1d0072`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948476976b5affd175205c3463e19547505c660c8d62ec0c51a0ccab24e7a100`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3066dd587e2e5fd44cc77bcf785a1eda6cb2c8fbfea705e112683712dc9bbf45`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de535d017baa9a7dbbcba70d7fde8cdb8607907fd1752fa99946ddf57958b2b0`  
		Last Modified: Thu, 15 Feb 2024 02:08:00 GMT  
		Size: 250.5 MB (250507125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1858c84143178e070fff903c762901603d1b1356e962f4fb73a71a200a55c84c`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore`

```console
$ docker pull julia@sha256:91949f9dc6a2ba335f38712cd941eb739d1c64a260fde1059319857eab40e0e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

### `julia:windowsservercore` - windows version 10.0.20348.2322; amd64

```console
$ docker pull julia@sha256:ac7e7de1919e6a391278fd06062034d24dd1892f6569260439ea7a8aac745dd0
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2161166383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f26f77914b415046af8c139841e565707106b2048fc516c6c1cb8347d2a4f8`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Thu, 15 Feb 2024 01:55:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 15 Feb 2024 01:55:58 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 01:55:58 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.1-win64.exe
# Thu, 15 Feb 2024 01:55:59 GMT
ENV JULIA_SHA256=ca02e6bd4f771d51c72520f359d727679775c03f62e7e7e2595dd79d1d0e5fec
# Thu, 15 Feb 2024 01:57:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 15 Feb 2024 01:57:04 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ecd8f02f1b59d6f3aec1c570f2c8128d2b064a59e0da86653fdee442a472ad`  
		Last Modified: Thu, 15 Feb 2024 01:57:11 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62852f81701e842eaa34fb5baf41629e3a8bd717a09aeae6c9d8f85aa6d3d870`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a1387c2ad061bd6ecc5941ab04b037b84018b2bfddaa265150d148ffca73b4`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f3360ff5dce5375b4b898a4f4deb9f588e12659cb8db5611d7e3e01952b012`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44ebaee761d2302e12dcc0f6dc0d9e5debeb07658857a8749c1f96a07fa3bfb`  
		Last Modified: Thu, 15 Feb 2024 01:58:16 GMT  
		Size: 250.5 MB (250505768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c23a6fdc0fc3d51f4f3676cdf3a438f7d52cb9f9a6a964c4645f304cf900ff`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:windowsservercore` - windows version 10.0.17763.5458; amd64

```console
$ docker pull julia@sha256:0955c5756b87875173c9a5b65b2df8cbb7d5b390c9c4550f7f521c40b3fa1935
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2330962381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef0a0692cd89c0ebd705bcc2f6c2ddf0fa8c2f800111fbf1041ec324ce62832a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Thu, 15 Feb 2024 02:05:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 15 Feb 2024 02:05:41 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 02:05:42 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.1-win64.exe
# Thu, 15 Feb 2024 02:05:43 GMT
ENV JULIA_SHA256=ca02e6bd4f771d51c72520f359d727679775c03f62e7e7e2595dd79d1d0e5fec
# Thu, 15 Feb 2024 02:07:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 15 Feb 2024 02:07:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ed3e36144d60ff8117a3dd6eb64daa4e29953bb129aaad397b30092f9cc4c1`  
		Last Modified: Thu, 15 Feb 2024 02:07:25 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ff9d169a5e63801023c2b6a0a537977e5c7505d96e3c8896d7dfeadf1d0072`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948476976b5affd175205c3463e19547505c660c8d62ec0c51a0ccab24e7a100`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3066dd587e2e5fd44cc77bcf785a1eda6cb2c8fbfea705e112683712dc9bbf45`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de535d017baa9a7dbbcba70d7fde8cdb8607907fd1752fa99946ddf57958b2b0`  
		Last Modified: Thu, 15 Feb 2024 02:08:00 GMT  
		Size: 250.5 MB (250507125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1858c84143178e070fff903c762901603d1b1356e962f4fb73a71a200a55c84c`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore-1809`

```console
$ docker pull julia@sha256:8720bbebce56e70f307b6ac3cd3d43e9f56b62fb168aade64cdb8abadc92f745
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `julia:windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull julia@sha256:0955c5756b87875173c9a5b65b2df8cbb7d5b390c9c4550f7f521c40b3fa1935
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2330962381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef0a0692cd89c0ebd705bcc2f6c2ddf0fa8c2f800111fbf1041ec324ce62832a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Thu, 15 Feb 2024 02:05:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 15 Feb 2024 02:05:41 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 02:05:42 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.1-win64.exe
# Thu, 15 Feb 2024 02:05:43 GMT
ENV JULIA_SHA256=ca02e6bd4f771d51c72520f359d727679775c03f62e7e7e2595dd79d1d0e5fec
# Thu, 15 Feb 2024 02:07:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 15 Feb 2024 02:07:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ed3e36144d60ff8117a3dd6eb64daa4e29953bb129aaad397b30092f9cc4c1`  
		Last Modified: Thu, 15 Feb 2024 02:07:25 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ff9d169a5e63801023c2b6a0a537977e5c7505d96e3c8896d7dfeadf1d0072`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948476976b5affd175205c3463e19547505c660c8d62ec0c51a0ccab24e7a100`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3066dd587e2e5fd44cc77bcf785a1eda6cb2c8fbfea705e112683712dc9bbf45`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de535d017baa9a7dbbcba70d7fde8cdb8607907fd1752fa99946ddf57958b2b0`  
		Last Modified: Thu, 15 Feb 2024 02:08:00 GMT  
		Size: 250.5 MB (250507125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1858c84143178e070fff903c762901603d1b1356e962f4fb73a71a200a55c84c`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:9a0e4ffc6087aabba7828052356da4cfbfb1db8f47eba6afec0c6bf93a96f3a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2322; amd64

### `julia:windowsservercore-ltsc2022` - windows version 10.0.20348.2322; amd64

```console
$ docker pull julia@sha256:ac7e7de1919e6a391278fd06062034d24dd1892f6569260439ea7a8aac745dd0
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2161166383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f26f77914b415046af8c139841e565707106b2048fc516c6c1cb8347d2a4f8`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Thu, 15 Feb 2024 01:55:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 15 Feb 2024 01:55:58 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 01:55:58 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.1-win64.exe
# Thu, 15 Feb 2024 01:55:59 GMT
ENV JULIA_SHA256=ca02e6bd4f771d51c72520f359d727679775c03f62e7e7e2595dd79d1d0e5fec
# Thu, 15 Feb 2024 01:57:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 15 Feb 2024 01:57:04 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ecd8f02f1b59d6f3aec1c570f2c8128d2b064a59e0da86653fdee442a472ad`  
		Last Modified: Thu, 15 Feb 2024 01:57:11 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62852f81701e842eaa34fb5baf41629e3a8bd717a09aeae6c9d8f85aa6d3d870`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a1387c2ad061bd6ecc5941ab04b037b84018b2bfddaa265150d148ffca73b4`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f3360ff5dce5375b4b898a4f4deb9f588e12659cb8db5611d7e3e01952b012`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44ebaee761d2302e12dcc0f6dc0d9e5debeb07658857a8749c1f96a07fa3bfb`  
		Last Modified: Thu, 15 Feb 2024 01:58:16 GMT  
		Size: 250.5 MB (250505768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c23a6fdc0fc3d51f4f3676cdf3a438f7d52cb9f9a6a964c4645f304cf900ff`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
