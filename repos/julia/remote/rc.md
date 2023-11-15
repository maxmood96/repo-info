## `julia:rc`

```console
$ docker pull julia@sha256:de6e30db8a2f50f2a6cbaaa44dd2c46fc5648ff7bdf71904b33bdc2d99d48662
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.20348.2031; amd64
	-	windows version 10.0.17763.4974; amd64

### `julia:rc` - linux; amd64

```console
$ docker pull julia@sha256:d1873d64e2eb52c8811db5261e50e91e6cf6836474504f36f1a51578617ad58e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 MB (204986703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8379ccd3f1c608d80eb08c3e2105f6ae6f28fbdd0391d7b6df845e8eccd3f20a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:49 GMT
ADD file:fbd8521c24ed758023728505c18d7a0d6d101bc77fd772a4af9b65049b943864 in / 
# Wed, 01 Nov 2023 00:20:49 GMT
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
ENV JULIA_VERSION=1.10.0-rc1
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-rc1-linux-x86_64.tar.gz'; 			sha256='fab4b6ae9f39b0a59e4d98db73b563521716cdcfe34247638146f208a57a5b5b'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-rc1-linux-aarch64.tar.gz'; 			sha256='9388c0e8f16b19233a5a80d09d9f16cdb4f94c3b5f6ee9e0b6a0bf852299c30a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-rc1-linux-i686.tar.gz'; 			sha256='1c137371781d126d50871d394a70765ba610c8aaf2b70d0d87004c2e41e290e6'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0-rc1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0-rc1?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:578acb154839e9d0034432e8f53756d6f53ba62cf8c7ea5218a2476bf5b58fc9`  
		Last Modified: Wed, 01 Nov 2023 00:25:30 GMT  
		Size: 29.1 MB (29149836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410403c2fdc134a98fbaedefbf24d7111731b9f9059cd9be4d0b87c1c846a11e`  
		Last Modified: Wed, 15 Nov 2023 02:22:50 GMT  
		Size: 5.5 MB (5513958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5df1e616f6f1cb9947e7545f75af19ce3663b89aba30f6a49efe2dac854777`  
		Last Modified: Wed, 15 Nov 2023 02:22:53 GMT  
		Size: 170.3 MB (170322538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6a251ddf5033f8bcac77f34f8bae129859cfdd68052819932297de4dff4351`  
		Last Modified: Wed, 15 Nov 2023 02:22:49 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:bee310ef9d9a6cd0d5276c23cf8808f8c43bde9556f094aca72bc8440aae8c64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2120160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0e14894482273484bdbc8618d3ea645d2bb08a0cef6d13d7adfbc8dedecf6e5`

```dockerfile
```

-	Layers:
	-	`sha256:88893ea51b2e4942ae51c0fcd793b504ba12cc4773b93ffd433a35f25ab228f5`  
		Last Modified: Wed, 15 Nov 2023 02:22:50 GMT  
		Size: 2.1 MB (2101945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a6a9789a8e96ea27f1e8b238b99ed34198ea6e23af3e1d0231e4e85bbafd08d`  
		Last Modified: Wed, 15 Nov 2023 02:22:49 GMT  
		Size: 18.2 KB (18215 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:32006364a120e4839f31c26df4edb4a40ce134b7ee3715669df5d94f3f4751be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199082072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02040c10b0b44a2489918d41d46d619d035e21782dbad4f7738991422f7b9a15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:41 GMT
ADD file:c58f86cd28b3a97f884e2a46f8fe60a2c5c1f443e198bd10e3277b4f3653736a in / 
# Wed, 01 Nov 2023 00:39:41 GMT
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
ENV JULIA_VERSION=1.10.0-rc1
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-rc1-linux-x86_64.tar.gz'; 			sha256='fab4b6ae9f39b0a59e4d98db73b563521716cdcfe34247638146f208a57a5b5b'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-rc1-linux-aarch64.tar.gz'; 			sha256='9388c0e8f16b19233a5a80d09d9f16cdb4f94c3b5f6ee9e0b6a0bf852299c30a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-rc1-linux-i686.tar.gz'; 			sha256='1c137371781d126d50871d394a70765ba610c8aaf2b70d0d87004c2e41e290e6'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0-rc1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0-rc1?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:31ce7ceb6d443e2ab4ae91695fea10e1443417fd94c40a46994d5a96940ea1ca`  
		Last Modified: Wed, 01 Nov 2023 00:43:07 GMT  
		Size: 29.2 MB (29179119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b96c9ec60fa5276c3bf23baa4892cc9ef71bb23f98cc26493b3708481efaac`  
		Last Modified: Thu, 02 Nov 2023 04:07:58 GMT  
		Size: 5.3 MB (5339550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53086ab0fe952feacb9edf367379f43bb4d0e0bd9390561ec977ec6fcd85a0df`  
		Last Modified: Wed, 15 Nov 2023 07:45:41 GMT  
		Size: 164.6 MB (164563034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e1bd5cb3f204b158080e2dbb706f85a0b5a6b0d7d76762be0290ffc71201cc`  
		Last Modified: Wed, 15 Nov 2023 07:45:37 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:580787379c85f0c1e8c833a47697930985cf87d028c26196a2edf72c9cef6037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2120345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba6bb3ccdb33cc10a269ae9a7e2a111260bdb93eb72f9cfe21a03bb404cab128`

```dockerfile
```

-	Layers:
	-	`sha256:d6636ce108737058d23e82bb19310ef1c2a3417a6b0c5fd34f48f625bdc8a685`  
		Last Modified: Wed, 15 Nov 2023 07:45:37 GMT  
		Size: 2.1 MB (2102284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fa74ae5ad87ab6eadcd70a11a3feff961388b13ffcf110721684d8b6d54fe9e`  
		Last Modified: Wed, 15 Nov 2023 07:45:37 GMT  
		Size: 18.1 KB (18061 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - linux; 386

```console
$ docker pull julia@sha256:716e2615effba9ea4223a2bbd208b75bbc47914782548c3b8c673b787afa1323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.3 MB (192323147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8c3652393716746584ebbb785f16383eaec547b2816f12f226e392cd1831d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 01 Nov 2023 00:38:56 GMT
ADD file:0c94521fdd9c0a4fdeeb9aad23e68cd053fba0dcd7c3af550aefa79377816e31 in / 
# Wed, 01 Nov 2023 00:38:56 GMT
CMD ["bash"]
# Sat, 04 Nov 2023 05:59:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 04 Nov 2023 05:59:13 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 04 Nov 2023 05:59:13 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Nov 2023 05:59:13 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 04 Nov 2023 05:59:13 GMT
ENV JULIA_VERSION=1.10.0-rc1
# Sat, 04 Nov 2023 05:59:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-rc1-linux-x86_64.tar.gz'; 			sha256='fab4b6ae9f39b0a59e4d98db73b563521716cdcfe34247638146f208a57a5b5b'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-rc1-linux-aarch64.tar.gz'; 			sha256='9388c0e8f16b19233a5a80d09d9f16cdb4f94c3b5f6ee9e0b6a0bf852299c30a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-rc1-linux-i686.tar.gz'; 			sha256='1c137371781d126d50871d394a70765ba610c8aaf2b70d0d87004c2e41e290e6'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sat, 04 Nov 2023 05:59:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 04 Nov 2023 05:59:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 04 Nov 2023 05:59:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:98bdfce9af831c2a0d0bfcca812d0039cd1666986550f552b4b4c625bd5aa31c`  
		Last Modified: Wed, 01 Nov 2023 00:43:26 GMT  
		Size: 30.2 MB (30164042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb25f9a1816a54d9e25b3b81c16d684f56cda2f7638000ac5eddf8161a0e319`  
		Last Modified: Wed, 08 Nov 2023 00:03:38 GMT  
		Size: 5.7 MB (5669500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165637906e46c2b0b21fa0968f7f200d4f3bcc739c50c1cc6b67d50802f68f20`  
		Last Modified: Wed, 08 Nov 2023 00:03:46 GMT  
		Size: 156.5 MB (156489236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1ef71d1bba35e292639d64f8a213239e049bcbd25e47ea207572f74633e1cc`  
		Last Modified: Wed, 08 Nov 2023 00:03:38 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:6135e9d76519b4297770570657d54621fea7980b4570c4f7ee460dd41df4a642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 KB (16895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c7c8217b6c6dbfbd763f37212080f01ae14b4eda5f8e506ec47dbcb2844df34`

```dockerfile
```

-	Layers:
	-	`sha256:91431df98d86754da937ebc2acbe0c5931ed40cf8e33c1f4e1b23450f0e2998f`  
		Last Modified: Wed, 08 Nov 2023 00:03:37 GMT  
		Size: 16.9 KB (16895 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - windows version 10.0.20348.2031; amd64

```console
$ docker pull julia@sha256:fa6dfb0f77c497d164586018f0110a596df07dbeaa62ae8b6ed9e264181bf400
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2041641349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ae718649b8fcee05be6c3fd98367eb03bf8febb55db57ff20dea047fca05ba9`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 06 Oct 2023 21:59:31 GMT
RUN Install update 10.0.20348.2031
# Wed, 11 Oct 2023 01:35:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 05:57:27 GMT
ENV JULIA_VERSION=1.10.0-beta3
# Wed, 11 Oct 2023 05:57:27 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.0-beta3-win64.exe
# Wed, 11 Oct 2023 05:57:28 GMT
ENV JULIA_SHA256=bd27c28ed52d4ec9985f90c649271b73fbd8048390c75b63fb329ebc9ed8e5c7
# Wed, 11 Oct 2023 05:58:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Oct 2023 05:58:49 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d2471a50c8ec3ea61c16dd871f7b9167bf779faad2b6e5a6f72a18b88b846b`  
		Last Modified: Tue, 10 Oct 2023 17:55:23 GMT  
		Size: 471.2 MB (471244358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a73b90f34f44bbbb354af4f3d4cc6cde597d2f5183641e139f7ca8b76ec3bb9`  
		Last Modified: Wed, 11 Oct 2023 02:45:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c352e7f1c2b96ac5e78f293c884f24d3705f26bebdb7687c355f84381d9902c3`  
		Last Modified: Wed, 11 Oct 2023 06:09:05 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f13c765a9742ab4185fe4934805396c5361ecbb16cc59e9a080c93b116e165a`  
		Last Modified: Wed, 11 Oct 2023 06:09:06 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b283aac2369936ed249e2c218e9c33d33bfcd4f8d9e37d1b3fc63993a87fd2`  
		Last Modified: Wed, 11 Oct 2023 06:09:05 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e7b0654004031381aad81a575e8b527cd0add8bb0738785480bd977aa5b33d`  
		Last Modified: Wed, 11 Oct 2023 06:09:42 GMT  
		Size: 181.8 MB (181791733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc1f629e41cdefd2e67e1c1b14a678768c06e00171878b5e22039da21df47ee`  
		Last Modified: Wed, 11 Oct 2023 06:09:05 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc` - windows version 10.0.17763.4974; amd64

```console
$ docker pull julia@sha256:5c77bcf2800d578809c9015e5dd4aa670a30ff580fdeb9baa55b507e7f0edede
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2213409169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a0930b3ea5fced2545351e828048cc955dccb8b280768480a15a919928393f5`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 01:36:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 05:59:10 GMT
ENV JULIA_VERSION=1.10.0-beta3
# Wed, 11 Oct 2023 05:59:11 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.0-beta3-win64.exe
# Wed, 11 Oct 2023 05:59:11 GMT
ENV JULIA_SHA256=bd27c28ed52d4ec9985f90c649271b73fbd8048390c75b63fb329ebc9ed8e5c7
# Wed, 11 Oct 2023 06:01:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Oct 2023 06:01:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0814e4a0bb8c615854a85a2b60cd043cfd20ad5a5d755acab1b30b18e4bfad3c`  
		Last Modified: Wed, 11 Oct 2023 02:46:41 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5fd91140cfa6cafb1eb8795b48e354160478a29bf49f6533bcfb61605e5e31f`  
		Last Modified: Wed, 11 Oct 2023 06:09:53 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d262baca50ad9492cc7ffdc50037a2ac2e28f3ac7bd45b5a523b86d392dc54`  
		Last Modified: Wed, 11 Oct 2023 06:09:53 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81845909255d6f75854314b9ea37ab1357f8ef420f2cd957e52b67c6db8b0874`  
		Last Modified: Wed, 11 Oct 2023 06:09:53 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec495184b422075f73bd4d76404193b02e7b6b738f9fb9ab98dfe948bd3dddf`  
		Last Modified: Wed, 11 Oct 2023 06:10:32 GMT  
		Size: 181.8 MB (181812014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4666bc0a41fa64b8fd5b72f083cc1f798e99e4ea121acd8222bab60d64973c42`  
		Last Modified: Wed, 11 Oct 2023 06:09:53 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
