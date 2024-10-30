<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `julia`

-	[`julia:1`](#julia1)
-	[`julia:1-bookworm`](#julia1-bookworm)
-	[`julia:1-bullseye`](#julia1-bullseye)
-	[`julia:1-windowsservercore`](#julia1-windowsservercore)
-	[`julia:1-windowsservercore-1809`](#julia1-windowsservercore-1809)
-	[`julia:1-windowsservercore-ltsc2022`](#julia1-windowsservercore-ltsc2022)
-	[`julia:1.10`](#julia110)
-	[`julia:1.10-alpine`](#julia110-alpine)
-	[`julia:1.10-alpine3.19`](#julia110-alpine319)
-	[`julia:1.10-alpine3.20`](#julia110-alpine320)
-	[`julia:1.10-bookworm`](#julia110-bookworm)
-	[`julia:1.10-bullseye`](#julia110-bullseye)
-	[`julia:1.10-windowsservercore`](#julia110-windowsservercore)
-	[`julia:1.10-windowsservercore-1809`](#julia110-windowsservercore-1809)
-	[`julia:1.10-windowsservercore-ltsc2022`](#julia110-windowsservercore-ltsc2022)
-	[`julia:1.10.6`](#julia1106)
-	[`julia:1.10.6-alpine`](#julia1106-alpine)
-	[`julia:1.10.6-alpine3.19`](#julia1106-alpine319)
-	[`julia:1.10.6-alpine3.20`](#julia1106-alpine320)
-	[`julia:1.10.6-bookworm`](#julia1106-bookworm)
-	[`julia:1.10.6-bullseye`](#julia1106-bullseye)
-	[`julia:1.10.6-windowsservercore`](#julia1106-windowsservercore)
-	[`julia:1.10.6-windowsservercore-1809`](#julia1106-windowsservercore-1809)
-	[`julia:1.10.6-windowsservercore-ltsc2022`](#julia1106-windowsservercore-ltsc2022)
-	[`julia:1.11`](#julia111)
-	[`julia:1.11-bookworm`](#julia111-bookworm)
-	[`julia:1.11-bullseye`](#julia111-bullseye)
-	[`julia:1.11-windowsservercore`](#julia111-windowsservercore)
-	[`julia:1.11-windowsservercore-1809`](#julia111-windowsservercore-1809)
-	[`julia:1.11-windowsservercore-ltsc2022`](#julia111-windowsservercore-ltsc2022)
-	[`julia:1.11.1`](#julia1111)
-	[`julia:1.11.1-bookworm`](#julia1111-bookworm)
-	[`julia:1.11.1-bullseye`](#julia1111-bullseye)
-	[`julia:1.11.1-windowsservercore`](#julia1111-windowsservercore)
-	[`julia:1.11.1-windowsservercore-1809`](#julia1111-windowsservercore-1809)
-	[`julia:1.11.1-windowsservercore-ltsc2022`](#julia1111-windowsservercore-ltsc2022)
-	[`julia:bookworm`](#juliabookworm)
-	[`julia:bullseye`](#juliabullseye)
-	[`julia:latest`](#julialatest)
-	[`julia:windowsservercore`](#juliawindowsservercore)
-	[`julia:windowsservercore-1809`](#juliawindowsservercore-1809)
-	[`julia:windowsservercore-ltsc2022`](#juliawindowsservercore-ltsc2022)

## `julia:1`

```console
$ docker pull julia@sha256:59ccf7b59abf7f7d78813b5fb0e244b0c7830c5656b956f9fde7bd27626476c0
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
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `julia:1` - linux; amd64

```console
$ docker pull julia@sha256:fd3a4e95d341cae23b3aef5fcf9fec1d2ee96fd1f1e3bcd6aa64643563ae314f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291937349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ea47312db572c60c8c9351c6b9a422aea6833da9717e5db4e3ea5f32f51b2dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
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
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bb87bd1b2a94a1a42597777f17fe57ac41a63e9ac4631763f29cc1c4eb7971`  
		Last Modified: Thu, 17 Oct 2024 01:21:28 GMT  
		Size: 5.7 MB (5712680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4115daba408d4d475ca265cb576361ce9cf9b002176e4268ae5a0b3eb9853f`  
		Last Modified: Thu, 17 Oct 2024 01:21:36 GMT  
		Size: 257.1 MB (257098011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dff1f91cca18ab23d091ade6d0b0385a0c6050a8fc43fb5a8159e253ae8121b`  
		Last Modified: Thu, 17 Oct 2024 01:21:28 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:57ae5db18ee250b23a45ccc6fdfd5ccfee4d8c87efaf4d1abd057f2769a0329c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2453853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4337eaa6caa92128ea6fc9c7c22d4a311aa67f379c859d92b14a3d50d64a8df7`

```dockerfile
```

-	Layers:
	-	`sha256:63f5d166f6304023b2c389e225252262af1d10b62688335ff269f55508f042ec`  
		Last Modified: Thu, 17 Oct 2024 01:21:28 GMT  
		Size: 2.4 MB (2435621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:065c1f726a44cdf9df5e738e56cd81c29b434fbd47bd7d3361c1137f08dd4cfd`  
		Last Modified: Thu, 17 Oct 2024 01:21:28 GMT  
		Size: 18.2 KB (18232 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:a2491aa90ba329dafe060d6adb24cb3fb83e36f4c4286633692e583097db3c36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.7 MB (288700700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4129f7f55b30d16e8139c69a813236f23e65139288d9ee0075399d5f6b89e8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
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
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f005b595846e0cdd9b8d61bffb35f19c8e42003b09c6fa5d02f40d76d40d3142`  
		Last Modified: Thu, 17 Oct 2024 13:15:23 GMT  
		Size: 5.5 MB (5537166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c05e13caa8823e23d317536ff1d1dd1796fe2a83847ee02d6db48a22ba0646a`  
		Last Modified: Thu, 17 Oct 2024 13:15:28 GMT  
		Size: 254.0 MB (254006821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a62b6e4f6fa18765799cd22bcbae3f15f20072e9ae053bbdf98a3efe82f52df`  
		Last Modified: Thu, 17 Oct 2024 13:15:23 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:e36e79625d4b2f06ab1b7414a9487e294e789f55949c056a20ab07b607eebe13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2454336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8494e45d3412b161773bf9c522b57e83aa21c819be146fb56574805aae74dfcf`

```dockerfile
```

-	Layers:
	-	`sha256:e348b3b6b5b4e6f22acb995010c94ad138b49e91b49459d7330ea9c665239067`  
		Last Modified: Thu, 17 Oct 2024 13:15:23 GMT  
		Size: 2.4 MB (2435943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f241bd181640f964b873b1a39186238e3c1e3853e6238c3a768fc63f04bd97fc`  
		Last Modified: Thu, 17 Oct 2024 13:15:23 GMT  
		Size: 18.4 KB (18393 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - linux; 386

```console
$ docker pull julia@sha256:9664f1d3532459c67196e66b0da1c613348bb1cf1a7dc1c9db5e84315309012c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270672761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e604fb4f328efb8dfd2637df284176512ed1ed6b6c31def9ebcf21aec0c2b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
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
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef46da67fc6417b2c8511177a2f904986a28c82f5f3980c4a3bdda412a0cb96`  
		Last Modified: Thu, 17 Oct 2024 01:21:34 GMT  
		Size: 5.9 MB (5870476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8aa1a2f42b1e06e545c1b61c842a6ba6a571d450dcdddb64e06db764fe22c5c`  
		Last Modified: Thu, 17 Oct 2024 01:21:41 GMT  
		Size: 234.7 MB (234657651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5922d12011579acdb276facae35eb217cd417b8ec2ca21c0b5425fbce9957824`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:5eb0819bd9c824da83af57c0bc587134d66e1189b39e553b460a89a42bdffc69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2450874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4631426bd2f8080a85a75feec2e4cf79652d64624da9905f16d08a1587d6ad79`

```dockerfile
```

-	Layers:
	-	`sha256:fafe3fc46d504391631a308525c4ffbde1b21fc417b2faec508a98df7b15e1ee`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 2.4 MB (2432693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8863f51017c0640fb041800f19fb46fdfab92ec6c3729f6040e84fe38b66c4ed`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 18.2 KB (18181 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - linux; ppc64le

```console
$ docker pull julia@sha256:f1ffa4874e6d100fc1fdce7ae8cff75b4e3cddc3a7063b68467942ab0e7b2d8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.8 MB (283845662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad3f11c30a7d695a2d9d6b9c71b233a341fa06c2f6602447727e3a85aedab3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
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
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ce3688624a92ce5984769ec19a8b421d5cbfdd057e1e30bf5e57cada049215`  
		Last Modified: Thu, 17 Oct 2024 08:42:06 GMT  
		Size: 6.2 MB (6247943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a24702a300837b63b3c298602a67686d45b25deb56363aa065d299c9bdd29b1`  
		Last Modified: Thu, 17 Oct 2024 08:42:14 GMT  
		Size: 244.5 MB (244475147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a582dd71509d2a88c872a94ed8a67e73c053144e9c5664720588c7684748c068`  
		Last Modified: Thu, 17 Oct 2024 08:42:05 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:d6cbf0fa8a4870af9ee3181a941d82be8d58199b70f220a63dd91c918affbbde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2458348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa065e6917f5d7c47bd2416298a0c99812e31e2ddaa68483848ff93690e8f736`

```dockerfile
```

-	Layers:
	-	`sha256:3abe2457e038cfc98e2170b01d92cd1b40f47bfa8cf991cc1220a0da68f000d7`  
		Last Modified: Thu, 17 Oct 2024 08:42:06 GMT  
		Size: 2.4 MB (2440052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4312eae9f6f8c06593b79106a3f06b6ce65b15ecf3c05fce5aba31afba073be7`  
		Last Modified: Thu, 17 Oct 2024 08:42:05 GMT  
		Size: 18.3 KB (18296 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - windows version 10.0.20348.2762; amd64

```console
$ docker pull julia@sha256:1aadbfaaaab1ead9b289075e1c50a66c24e73f0abb54ff58987658fb3d721339
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2052417149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73d77c77c9074ad1a6ef6af5f3c75625db9c5be5d552e03bdfb712643fa3262`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Thu, 17 Oct 2024 00:07:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:07:44 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:07:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:07:46 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:09:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:09:05 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7310b1b784f497ecef75a191c3fdf858c6c5e7102326517af7e9c8f4a9ba2ab`  
		Last Modified: Thu, 17 Oct 2024 00:09:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8f60354745986b41d1c97227046f1bf77a40a1b841e2b733d28d9f336d0517a`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81f4ad3b9ee5bb6c5bcf302663adf9404aed5f2a775c97739ddeaf04c390105`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e95309645bd9402810abb1f62e8d28e2eb50ad30d923ac5635718caafc953f3`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1f65e1c7b97054a3ff76d9eb10192f3ffb9f984e554d5dad56b1deffa4a26e`  
		Last Modified: Thu, 17 Oct 2024 00:09:40 GMT  
		Size: 253.1 MB (253069135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3efcc69a49a46842179fb8d2b256e3aca046c05572afb9537e9e68808da649`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1` - windows version 10.0.17763.6414; amd64

```console
$ docker pull julia@sha256:5f7b3fa057a3f34c286a0c29544e30b8e25de7d389fcb9a7c39e5dbc2ac59431
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2154909599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73428e1a2c97df8e870d60c63531878514df329661819a1917855fe9c852deb3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Thu, 17 Oct 2024 00:04:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:04:47 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:06:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:06:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4316cb4a890d1430c8dbb6f02f1ed4b07cc1f84668ddfe58d132e70173591231`  
		Last Modified: Thu, 17 Oct 2024 00:06:49 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed07735f2e4d115dbc648a3fbf628ee5e173125dcd63d695a85f30c2d701668d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02cf70042980e2e6296807674462b486e411ba5e80ecf7c6ec3bdd5e0e7a5085`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1c8839b71fde8692b035b2f54ea4a7c21650e10ae20680a0ba68b723b9e57d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4afde2ddc271e774c969b81b72e4ec22aa664487988ca09a851e16930efb47`  
		Last Modified: Thu, 17 Oct 2024 00:07:18 GMT  
		Size: 253.1 MB (253077851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f694e951fd639e6dc35a1e43dce74e5247712830c183397156d8b0ff48747470`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-bookworm`

```console
$ docker pull julia@sha256:33cde3f7aaea90daa3bbb93d1a002daf679b68380a9cc24420b90e2c88382d36
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
$ docker pull julia@sha256:fd3a4e95d341cae23b3aef5fcf9fec1d2ee96fd1f1e3bcd6aa64643563ae314f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291937349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ea47312db572c60c8c9351c6b9a422aea6833da9717e5db4e3ea5f32f51b2dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
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
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bb87bd1b2a94a1a42597777f17fe57ac41a63e9ac4631763f29cc1c4eb7971`  
		Last Modified: Thu, 17 Oct 2024 01:21:28 GMT  
		Size: 5.7 MB (5712680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4115daba408d4d475ca265cb576361ce9cf9b002176e4268ae5a0b3eb9853f`  
		Last Modified: Thu, 17 Oct 2024 01:21:36 GMT  
		Size: 257.1 MB (257098011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dff1f91cca18ab23d091ade6d0b0385a0c6050a8fc43fb5a8159e253ae8121b`  
		Last Modified: Thu, 17 Oct 2024 01:21:28 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:57ae5db18ee250b23a45ccc6fdfd5ccfee4d8c87efaf4d1abd057f2769a0329c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2453853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4337eaa6caa92128ea6fc9c7c22d4a311aa67f379c859d92b14a3d50d64a8df7`

```dockerfile
```

-	Layers:
	-	`sha256:63f5d166f6304023b2c389e225252262af1d10b62688335ff269f55508f042ec`  
		Last Modified: Thu, 17 Oct 2024 01:21:28 GMT  
		Size: 2.4 MB (2435621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:065c1f726a44cdf9df5e738e56cd81c29b434fbd47bd7d3361c1137f08dd4cfd`  
		Last Modified: Thu, 17 Oct 2024 01:21:28 GMT  
		Size: 18.2 KB (18232 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:a2491aa90ba329dafe060d6adb24cb3fb83e36f4c4286633692e583097db3c36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.7 MB (288700700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4129f7f55b30d16e8139c69a813236f23e65139288d9ee0075399d5f6b89e8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
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
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f005b595846e0cdd9b8d61bffb35f19c8e42003b09c6fa5d02f40d76d40d3142`  
		Last Modified: Thu, 17 Oct 2024 13:15:23 GMT  
		Size: 5.5 MB (5537166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c05e13caa8823e23d317536ff1d1dd1796fe2a83847ee02d6db48a22ba0646a`  
		Last Modified: Thu, 17 Oct 2024 13:15:28 GMT  
		Size: 254.0 MB (254006821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a62b6e4f6fa18765799cd22bcbae3f15f20072e9ae053bbdf98a3efe82f52df`  
		Last Modified: Thu, 17 Oct 2024 13:15:23 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:e36e79625d4b2f06ab1b7414a9487e294e789f55949c056a20ab07b607eebe13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2454336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8494e45d3412b161773bf9c522b57e83aa21c819be146fb56574805aae74dfcf`

```dockerfile
```

-	Layers:
	-	`sha256:e348b3b6b5b4e6f22acb995010c94ad138b49e91b49459d7330ea9c665239067`  
		Last Modified: Thu, 17 Oct 2024 13:15:23 GMT  
		Size: 2.4 MB (2435943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f241bd181640f964b873b1a39186238e3c1e3853e6238c3a768fc63f04bd97fc`  
		Last Modified: Thu, 17 Oct 2024 13:15:23 GMT  
		Size: 18.4 KB (18393 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; 386

```console
$ docker pull julia@sha256:9664f1d3532459c67196e66b0da1c613348bb1cf1a7dc1c9db5e84315309012c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270672761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e604fb4f328efb8dfd2637df284176512ed1ed6b6c31def9ebcf21aec0c2b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
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
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef46da67fc6417b2c8511177a2f904986a28c82f5f3980c4a3bdda412a0cb96`  
		Last Modified: Thu, 17 Oct 2024 01:21:34 GMT  
		Size: 5.9 MB (5870476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8aa1a2f42b1e06e545c1b61c842a6ba6a571d450dcdddb64e06db764fe22c5c`  
		Last Modified: Thu, 17 Oct 2024 01:21:41 GMT  
		Size: 234.7 MB (234657651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5922d12011579acdb276facae35eb217cd417b8ec2ca21c0b5425fbce9957824`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:5eb0819bd9c824da83af57c0bc587134d66e1189b39e553b460a89a42bdffc69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2450874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4631426bd2f8080a85a75feec2e4cf79652d64624da9905f16d08a1587d6ad79`

```dockerfile
```

-	Layers:
	-	`sha256:fafe3fc46d504391631a308525c4ffbde1b21fc417b2faec508a98df7b15e1ee`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 2.4 MB (2432693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8863f51017c0640fb041800f19fb46fdfab92ec6c3729f6040e84fe38b66c4ed`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 18.2 KB (18181 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:f1ffa4874e6d100fc1fdce7ae8cff75b4e3cddc3a7063b68467942ab0e7b2d8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.8 MB (283845662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad3f11c30a7d695a2d9d6b9c71b233a341fa06c2f6602447727e3a85aedab3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
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
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ce3688624a92ce5984769ec19a8b421d5cbfdd057e1e30bf5e57cada049215`  
		Last Modified: Thu, 17 Oct 2024 08:42:06 GMT  
		Size: 6.2 MB (6247943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a24702a300837b63b3c298602a67686d45b25deb56363aa065d299c9bdd29b1`  
		Last Modified: Thu, 17 Oct 2024 08:42:14 GMT  
		Size: 244.5 MB (244475147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a582dd71509d2a88c872a94ed8a67e73c053144e9c5664720588c7684748c068`  
		Last Modified: Thu, 17 Oct 2024 08:42:05 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:d6cbf0fa8a4870af9ee3181a941d82be8d58199b70f220a63dd91c918affbbde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2458348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa065e6917f5d7c47bd2416298a0c99812e31e2ddaa68483848ff93690e8f736`

```dockerfile
```

-	Layers:
	-	`sha256:3abe2457e038cfc98e2170b01d92cd1b40f47bfa8cf991cc1220a0da68f000d7`  
		Last Modified: Thu, 17 Oct 2024 08:42:06 GMT  
		Size: 2.4 MB (2440052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4312eae9f6f8c06593b79106a3f06b6ce65b15ecf3c05fce5aba31afba073be7`  
		Last Modified: Thu, 17 Oct 2024 08:42:05 GMT  
		Size: 18.3 KB (18296 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1-bullseye`

```console
$ docker pull julia@sha256:d8596315fc3f33f87595593bf6d6c24e7175f1ba2247551b566d73824426057e
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
$ docker pull julia@sha256:89b0252e81fcee8a8295a302dfbd5333ebf5fc9b2bbcbf21dd0dd432df83bd5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (290953918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c5e3b2a9d92441caccba1899fdfadb95145c7b3454af5d79cc49eef8a2b12dd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
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
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1678fe3cd4a658f476437fee9e77b0c2086786926a90c07b083d0343a3675d34`  
		Last Modified: Thu, 17 Oct 2024 01:21:31 GMT  
		Size: 2.4 MB (2426579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13bf3dac7e14a600162ea26186e3f4f9e2eb67b797a698ca137e9bda78be3095`  
		Last Modified: Thu, 17 Oct 2024 01:21:34 GMT  
		Size: 257.1 MB (257098167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24eeabef1fc4078b2230b57296e3885ca5a8abe902842a963d54dd9229da645`  
		Last Modified: Thu, 17 Oct 2024 01:21:31 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:67cb263e6e9c5a8df2d07f56530084b32aa0fa18b9f54e1c70633d08ee81508f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e7a2b55d44957d73538f15728c85350a58a54b6670423e772b5052af5b609b`

```dockerfile
```

-	Layers:
	-	`sha256:e404b3ce366a6055b639f0e587f8f22d969c64c22ecac08b317416e03980c296`  
		Last Modified: Thu, 17 Oct 2024 01:21:31 GMT  
		Size: 2.7 MB (2703232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1cca66d1ab6aee6b83ad8e00220188da64a51b78924668d3a5d499b22c95b52`  
		Last Modified: Thu, 17 Oct 2024 01:21:31 GMT  
		Size: 17.1 KB (17061 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4f7f024b62a8f78c7294efa5ae1766b248b3bdf7b9bbb5e9c1416e4e8d1d84fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286497932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e390fcde5664778999f291f06fae01e77921743114fe33fdc45f3115c43c11dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
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
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a413099e7fe61ccf8c3081b040fa09c50cbc6a831480a5614a60a0d3c69b56b8`  
		Last Modified: Thu, 17 Oct 2024 13:16:53 GMT  
		Size: 2.4 MB (2415124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ec42daf214f0d308f8292a6037cc8f045cfdc9adfe28ff544cc0fb9a87b67a`  
		Last Modified: Thu, 17 Oct 2024 13:16:59 GMT  
		Size: 254.0 MB (254006680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a03157b90421e9af495118fb5dd03f42dc3a8de569955b88ad28a1def229884`  
		Last Modified: Thu, 17 Oct 2024 13:16:53 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:37c0ceb7fd6b428c7ce243fdeb9373c1099770d26ebc891187c07606979b3708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d376da6f82e6ccf88c0c94e1cd0081b3dd5ecd7135c4e0a073360dd2f42e4009`

```dockerfile
```

-	Layers:
	-	`sha256:379457b9725569536171521dfa577f8872f6d6231c665f670eb96bc047caa7e1`  
		Last Modified: Thu, 17 Oct 2024 13:16:53 GMT  
		Size: 2.7 MB (2703494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1b312173fb754b10124c5b9d4a848af7c804fd34ba816a297562afe8a0b0353`  
		Last Modified: Thu, 17 Oct 2024 13:16:53 GMT  
		Size: 17.2 KB (17174 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bullseye` - linux; 386

```console
$ docker pull julia@sha256:3670a732c97cffad25985d92fbb803b9b874eca1f6e26a4f56d8a77c91c1deea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.6 MB (269605951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bb8f95ee66c50d9e825aedeb3254da01eaa7c893aec91624b016ac95a35fe7c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD file:05098c6b0b4cfde8b4ffadc861fc7668bbf1779983d50b6be61989e6378fc17b in / 
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
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
	-	`sha256:0aff79075c186716daeb376e46e89131aa14f0dc2bd8f794bd04d72494cb4693`  
		Last Modified: Thu, 17 Oct 2024 00:43:15 GMT  
		Size: 32.4 MB (32413830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351b630321cf786277448e0f7aea94f99fc611feec697422839581d6ba78b0f4`  
		Last Modified: Thu, 17 Oct 2024 01:14:36 GMT  
		Size: 2.5 MB (2533097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a25ec52f239ad17072bdbca92923baca090ca0beb325e15e8b38ec0d9a07bb6`  
		Last Modified: Thu, 17 Oct 2024 01:14:41 GMT  
		Size: 234.7 MB (234658656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacaf77ce79d2cad5f10ebb5c0a2cf0132caef0f18a13b0397f5419a1b104dae`  
		Last Modified: Thu, 17 Oct 2024 01:14:36 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:801107f4fb9fa1d75ece047478ee52a0cde10e3e985cb4235e707647835d9385
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2717361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a242ec47f9cd91c5c05a334d40ffb11921f23481e6fca0e70c18cee75e1be40`

```dockerfile
```

-	Layers:
	-	`sha256:2a3f27893e3c035da08f3858e8b8d9e3d748d8c2d2a8354fba0c038570df9fc1`  
		Last Modified: Thu, 17 Oct 2024 01:14:36 GMT  
		Size: 2.7 MB (2700330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1c148b1faeb4d330bc4cb1657a099ca6c996d5624aa2a62d3c3945b9e70e713`  
		Last Modified: Thu, 17 Oct 2024 01:14:36 GMT  
		Size: 17.0 KB (17031 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1-windowsservercore`

```console
$ docker pull julia@sha256:d36dd547370e9fd68c4f5dc635f8c3ea0da809f71f508a8724c909f927574ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `julia:1-windowsservercore` - windows version 10.0.20348.2762; amd64

```console
$ docker pull julia@sha256:1aadbfaaaab1ead9b289075e1c50a66c24e73f0abb54ff58987658fb3d721339
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2052417149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73d77c77c9074ad1a6ef6af5f3c75625db9c5be5d552e03bdfb712643fa3262`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Thu, 17 Oct 2024 00:07:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:07:44 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:07:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:07:46 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:09:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:09:05 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7310b1b784f497ecef75a191c3fdf858c6c5e7102326517af7e9c8f4a9ba2ab`  
		Last Modified: Thu, 17 Oct 2024 00:09:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8f60354745986b41d1c97227046f1bf77a40a1b841e2b733d28d9f336d0517a`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81f4ad3b9ee5bb6c5bcf302663adf9404aed5f2a775c97739ddeaf04c390105`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e95309645bd9402810abb1f62e8d28e2eb50ad30d923ac5635718caafc953f3`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1f65e1c7b97054a3ff76d9eb10192f3ffb9f984e554d5dad56b1deffa4a26e`  
		Last Modified: Thu, 17 Oct 2024 00:09:40 GMT  
		Size: 253.1 MB (253069135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3efcc69a49a46842179fb8d2b256e3aca046c05572afb9537e9e68808da649`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull julia@sha256:5f7b3fa057a3f34c286a0c29544e30b8e25de7d389fcb9a7c39e5dbc2ac59431
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2154909599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73428e1a2c97df8e870d60c63531878514df329661819a1917855fe9c852deb3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Thu, 17 Oct 2024 00:04:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:04:47 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:06:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:06:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4316cb4a890d1430c8dbb6f02f1ed4b07cc1f84668ddfe58d132e70173591231`  
		Last Modified: Thu, 17 Oct 2024 00:06:49 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed07735f2e4d115dbc648a3fbf628ee5e173125dcd63d695a85f30c2d701668d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02cf70042980e2e6296807674462b486e411ba5e80ecf7c6ec3bdd5e0e7a5085`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1c8839b71fde8692b035b2f54ea4a7c21650e10ae20680a0ba68b723b9e57d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4afde2ddc271e774c969b81b72e4ec22aa664487988ca09a851e16930efb47`  
		Last Modified: Thu, 17 Oct 2024 00:07:18 GMT  
		Size: 253.1 MB (253077851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f694e951fd639e6dc35a1e43dce74e5247712830c183397156d8b0ff48747470`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore-1809`

```console
$ docker pull julia@sha256:a114dd8364b3c4135706a0b323f71e0e649bff9cf95ae8300f0378d0951c131e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `julia:1-windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull julia@sha256:5f7b3fa057a3f34c286a0c29544e30b8e25de7d389fcb9a7c39e5dbc2ac59431
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2154909599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73428e1a2c97df8e870d60c63531878514df329661819a1917855fe9c852deb3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Thu, 17 Oct 2024 00:04:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:04:47 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:06:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:06:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4316cb4a890d1430c8dbb6f02f1ed4b07cc1f84668ddfe58d132e70173591231`  
		Last Modified: Thu, 17 Oct 2024 00:06:49 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed07735f2e4d115dbc648a3fbf628ee5e173125dcd63d695a85f30c2d701668d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02cf70042980e2e6296807674462b486e411ba5e80ecf7c6ec3bdd5e0e7a5085`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1c8839b71fde8692b035b2f54ea4a7c21650e10ae20680a0ba68b723b9e57d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4afde2ddc271e774c969b81b72e4ec22aa664487988ca09a851e16930efb47`  
		Last Modified: Thu, 17 Oct 2024 00:07:18 GMT  
		Size: 253.1 MB (253077851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f694e951fd639e6dc35a1e43dce74e5247712830c183397156d8b0ff48747470`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:e457f763ca8c5fe3e8a20dd1a3cbf00134231b70f5070b6fa7ce67ff9536e8dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `julia:1-windowsservercore-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull julia@sha256:1aadbfaaaab1ead9b289075e1c50a66c24e73f0abb54ff58987658fb3d721339
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2052417149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73d77c77c9074ad1a6ef6af5f3c75625db9c5be5d552e03bdfb712643fa3262`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Thu, 17 Oct 2024 00:07:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:07:44 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:07:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:07:46 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:09:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:09:05 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7310b1b784f497ecef75a191c3fdf858c6c5e7102326517af7e9c8f4a9ba2ab`  
		Last Modified: Thu, 17 Oct 2024 00:09:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8f60354745986b41d1c97227046f1bf77a40a1b841e2b733d28d9f336d0517a`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81f4ad3b9ee5bb6c5bcf302663adf9404aed5f2a775c97739ddeaf04c390105`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e95309645bd9402810abb1f62e8d28e2eb50ad30d923ac5635718caafc953f3`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1f65e1c7b97054a3ff76d9eb10192f3ffb9f984e554d5dad56b1deffa4a26e`  
		Last Modified: Thu, 17 Oct 2024 00:09:40 GMT  
		Size: 253.1 MB (253069135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3efcc69a49a46842179fb8d2b256e3aca046c05572afb9537e9e68808da649`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10`

```console
$ docker pull julia@sha256:2e8a399601c766e397f9afdccb23dce25240605c48e59657947af3cfa3b80118
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
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `julia:1.10` - linux; amd64

```console
$ docker pull julia@sha256:066fe3c12ab811346b53168d4e6b894296b9c05c661f1160aaab7de42ba8db48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.5 MB (211469990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:650577d6aea7bd1e50734262e6250954dd8de23f0810f8e473d5b0b46ede003d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 17 Oct 2024 00:20:30 GMT
CMD ["bash"]
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.6-linux-x86_64.tar.gz'; 			sha256='8b53429e17585c66476b39f2b2279da207ea0f310c55db38f3410bdd4f6a3d49'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.6-linux-aarch64.tar.gz'; 			sha256='5530359839544ba1ee8f6f66728fd4f9b591822c1633f93cf9672c7f9528fc3a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.6-linux-i686.tar.gz'; 			sha256='52771086511905c22669bc8667a98a97ad26e82747a429165fde2641672e962b'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.6-linux-ppc64le.tar.gz'; 			sha256='bbfd63ba2bf497f82101ef8ca3e681adca4ab95f9d5e12abfb2cf3a3c72d6126'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24730e632d102308412e50d47afc4963ab80945853c21921db804fee91f70c4`  
		Last Modified: Tue, 29 Oct 2024 22:59:04 GMT  
		Size: 5.7 MB (5712693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54df6a7b1c987a3a57cf6c3a830c3d7ded854573b58fcbbc7c8ab5d975d3241b`  
		Last Modified: Tue, 29 Oct 2024 22:59:07 GMT  
		Size: 176.6 MB (176630637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f180184aba9526edbb4fa7be6a302a437d43b29f442ab8cd3062874fa38d52a1`  
		Last Modified: Tue, 29 Oct 2024 22:59:04 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:9cd8b3fc2a11d08112901e265156ad92fec39c16bd245987c402f1ecad86f33b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11687b4578ab84520d40c7e0c43a470aed5f538a5ca0b2db7132407d16805b63`

```dockerfile
```

-	Layers:
	-	`sha256:355f0872750dee81ec05047b47e309ca3afb653edcd42237934de5be5ecc1d73`  
		Last Modified: Tue, 29 Oct 2024 22:59:04 GMT  
		Size: 2.4 MB (2449212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18cccb85b4623e7a71d4bc6d3c361bc4642429b260ba99828e8b6398a6ace30e`  
		Last Modified: Tue, 29 Oct 2024 22:59:04 GMT  
		Size: 17.0 KB (17018 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:fe90cd54fa02a1a87cd43900e84872dac0e2eb6acb158a7df97cadf542412053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.0 MB (212041217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a349d4bb79aaa181d575d5c590ea369d89d19495483c28c89cc30ed9f22f9baa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.6-linux-x86_64.tar.gz'; 			sha256='8b53429e17585c66476b39f2b2279da207ea0f310c55db38f3410bdd4f6a3d49'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.6-linux-aarch64.tar.gz'; 			sha256='5530359839544ba1ee8f6f66728fd4f9b591822c1633f93cf9672c7f9528fc3a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.6-linux-i686.tar.gz'; 			sha256='52771086511905c22669bc8667a98a97ad26e82747a429165fde2641672e962b'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.6-linux-ppc64le.tar.gz'; 			sha256='bbfd63ba2bf497f82101ef8ca3e681adca4ab95f9d5e12abfb2cf3a3c72d6126'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9f7aa12a882cbec1989b7eb39edf886c46b6ec43a0dbdaa46322fb5ea3fd09`  
		Last Modified: Wed, 30 Oct 2024 00:03:43 GMT  
		Size: 5.5 MB (5537174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba2ee9345c139face9d10e01386b6012aa72822b7e356753ae9c5a875667fad`  
		Last Modified: Wed, 30 Oct 2024 00:03:47 GMT  
		Size: 177.3 MB (177347335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1623697d698db51239d0786367179ae5b9fdda3d9646d150726d51f4d05911`  
		Last Modified: Wed, 30 Oct 2024 00:03:42 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:0713eadec1bcf05f96c35d1be3349adfdba8398cd7e7141c0c397678f7199e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ef0d98ccdd9762f43506d01f867a1a6b49cbf1c69f3de0971422f25f8d61d5`

```dockerfile
```

-	Layers:
	-	`sha256:301ab6e57c61cb7bbd0857cd1cdc41631539edf83c6f8ed5e2116b5121b95800`  
		Last Modified: Wed, 30 Oct 2024 00:03:43 GMT  
		Size: 2.4 MB (2448264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:263e7cad0f4326e8b1f9b2a1bf2ad5ca2de932f3be76f4fcc153bbfeb6859c5b`  
		Last Modified: Wed, 30 Oct 2024 00:03:42 GMT  
		Size: 17.2 KB (17155 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; 386

```console
$ docker pull julia@sha256:c718d318da6995a7c5ed037813139bc5475763c90c69462b23a9c13f264071f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193827906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:142e4513d0ab21eb84ec458e70e790a6739e3398c6b63e4d2f7cf015259c8c9e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 17 Oct 2024 00:38:56 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Thu, 17 Oct 2024 00:38:56 GMT
CMD ["bash"]
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.6-linux-x86_64.tar.gz'; 			sha256='8b53429e17585c66476b39f2b2279da207ea0f310c55db38f3410bdd4f6a3d49'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.6-linux-aarch64.tar.gz'; 			sha256='5530359839544ba1ee8f6f66728fd4f9b591822c1633f93cf9672c7f9528fc3a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.6-linux-i686.tar.gz'; 			sha256='52771086511905c22669bc8667a98a97ad26e82747a429165fde2641672e962b'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.6-linux-ppc64le.tar.gz'; 			sha256='bbfd63ba2bf497f82101ef8ca3e681adca4ab95f9d5e12abfb2cf3a3c72d6126'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c544b64767c8ee9ec5202884260726a080b68fa738ff648f1936b53eb005db63`  
		Last Modified: Tue, 29 Oct 2024 22:59:02 GMT  
		Size: 5.9 MB (5870458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714cab6622ab2b57035ee3dbf90756fcc815ac79da12048a7416501899f30f15`  
		Last Modified: Tue, 29 Oct 2024 22:59:06 GMT  
		Size: 157.8 MB (157812811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135081bef526546ebd94b2b8c30a901dba8d23fb0d246f7784beecc4bcb2bf10`  
		Last Modified: Tue, 29 Oct 2024 22:59:02 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:bf6a8c8863c5670bf815c39bba3a0187df9dd2d04b885d1763f55fd9a169b1c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e27864b80a3b3c70874b2e512ecb8d105dc0ee3197d0e994acc19c4a3fbdc6e`

```dockerfile
```

-	Layers:
	-	`sha256:ec727e80c071bab5a789d0f27b0127857ca592daba008e3c2624602ffa12a9ed`  
		Last Modified: Tue, 29 Oct 2024 22:59:02 GMT  
		Size: 2.4 MB (2446304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8b8b1cbd3886057906d657ef37a305a39bc310e1a3cc8a9087fe2df9138a512`  
		Last Modified: Tue, 29 Oct 2024 22:59:02 GMT  
		Size: 17.0 KB (17011 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; ppc64le

```console
$ docker pull julia@sha256:c4c48e226ac08b9e19836392b0979936d62b3d7a36e84c5360d1d1b2b2d81547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.7 MB (194677985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17067b8f17bce468e0c9eeb8dc4f3ec6582dc539140ec4f27e41d606949f8b0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 17 Oct 2024 01:18:54 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Thu, 17 Oct 2024 01:18:56 GMT
CMD ["bash"]
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.6-linux-x86_64.tar.gz'; 			sha256='8b53429e17585c66476b39f2b2279da207ea0f310c55db38f3410bdd4f6a3d49'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.6-linux-aarch64.tar.gz'; 			sha256='5530359839544ba1ee8f6f66728fd4f9b591822c1633f93cf9672c7f9528fc3a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.6-linux-i686.tar.gz'; 			sha256='52771086511905c22669bc8667a98a97ad26e82747a429165fde2641672e962b'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.6-linux-ppc64le.tar.gz'; 			sha256='bbfd63ba2bf497f82101ef8ca3e681adca4ab95f9d5e12abfb2cf3a3c72d6126'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872ce7d06e1f062f97505b0e301bbfdbf0eb9be16d7514467915e735ab53c113`  
		Last Modified: Tue, 29 Oct 2024 23:01:05 GMT  
		Size: 6.2 MB (6247957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170dcc05149f98f3db1198fddc1be23f82b6ae0fcf50dd96e047466a8af395ac`  
		Last Modified: Tue, 29 Oct 2024 23:01:09 GMT  
		Size: 155.3 MB (155307456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbf0fac49cd21372305ab812b69a2b403d1f62371f492ce96e9f307669893dc`  
		Last Modified: Tue, 29 Oct 2024 23:01:04 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:605795e6f38be17a1fcaa2cfe024c183d09af212ccb061fa4ad2cf2d6b71b471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2469479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c724732b12d6ed77c9b813e7f50d05a34b89ea234bc8ceefbf789e5cf2ebcef0`

```dockerfile
```

-	Layers:
	-	`sha256:6f53f1adeb9f8fbab7623a47e3466557398985eb384c51887fbdfa6f9c1ca791`  
		Last Modified: Tue, 29 Oct 2024 23:01:05 GMT  
		Size: 2.5 MB (2452397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb684095369776335de241209d640d5a1f006b954d8abead862abffbbe157cf2`  
		Last Modified: Tue, 29 Oct 2024 23:01:04 GMT  
		Size: 17.1 KB (17082 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - windows version 10.0.20348.2762; amd64

```console
$ docker pull julia@sha256:0e742f15776e4f7e2466446691d4e7d0ae81576fea07e6ac69eea39d103d0173
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1988310186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3085046212c05c9e4b0a731e38e30128a7ac793956c2995e4417d66e1888e4b8`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Tue, 29 Oct 2024 23:56:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 29 Oct 2024 23:56:59 GMT
ENV JULIA_VERSION=1.10.6
# Tue, 29 Oct 2024 23:57:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.6-win64.exe
# Tue, 29 Oct 2024 23:57:02 GMT
ENV JULIA_SHA256=f29e62ea3edede6b9a245ca1117d5f5232a78f324902a69368e3ed5836f96d59
# Tue, 29 Oct 2024 23:59:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 29 Oct 2024 23:59:25 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a703ec8db6afe2491ab0518ad479df3ea9eb52d5967771bcebf035a59b29d6`  
		Last Modified: Tue, 29 Oct 2024 23:59:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8738f7e52db049fd38af00a87bd6e9119f5abbd70ab1bd552a1f01f9785c6b5d`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0083b70e021328f6ae7e9d213e77735279f1cf457c243584e8cea8bad89d18`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220778260973a205a267336a441e793360c94d727e8fce10de071e7edb0fa48b`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc4ea8989979e5b3bdf5bafb635c0dd5f91c792a52a23c77f353466f2dbeea3`  
		Last Modified: Tue, 29 Oct 2024 23:59:50 GMT  
		Size: 189.0 MB (188962205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ae0a51fc94fd2d69da5be3323e71e7737e28dd291e65c140e1836658098af0`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10` - windows version 10.0.17763.6414; amd64

```console
$ docker pull julia@sha256:6ca14732d9b63fca4b7397eadd040a3c87ccd84e1ba749fb7e1ee9bc42244913
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2090791615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d349843745bd27b77509eb661965f36217fa3b818dd96f5ef8ad5d5c868c8d93`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 29 Oct 2024 22:58:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 29 Oct 2024 22:58:31 GMT
ENV JULIA_VERSION=1.10.6
# Tue, 29 Oct 2024 22:58:32 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.6-win64.exe
# Tue, 29 Oct 2024 22:58:33 GMT
ENV JULIA_SHA256=f29e62ea3edede6b9a245ca1117d5f5232a78f324902a69368e3ed5836f96d59
# Tue, 29 Oct 2024 23:00:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 29 Oct 2024 23:00:38 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187f98b1f55258e314fedb9c2f6226e1c2a11740febbd0ce89d238e43c0bed2`  
		Last Modified: Tue, 29 Oct 2024 23:00:43 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba0606836b66ce8f497eac48f690ee807b532d6777b4e56ce704dd15e77e678a`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9b820753126ccfc32f3fba865e5d5b4824aedcdaf3831831d2844d43d919f6`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0726905f5fbf316e8c8c6741bc1793dde3958dca4f53a28ff39972d4253b31`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88eff14262dc220189629e33a16987149944ad23b1b5f939113fa634c51f7f4b`  
		Last Modified: Tue, 29 Oct 2024 23:01:04 GMT  
		Size: 189.0 MB (188959879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a37e9e4b5cd836f0416d006af1817bf06ea1be011782932bf2b3785e6a08c44`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-alpine`

```console
$ docker pull julia@sha256:5f547f1d17f11ca957b3246664002aee1365ad98e7437e28ff53b33f14fa9fff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10-alpine` - linux; amd64

```console
$ docker pull julia@sha256:64fd5bdc56499d4c38f939f6a40186b24cbd793cdfd0302d716bae656a0edfd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182832388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073e61618388a0ed05e82a4327440dfdbd3824aa763d09063f50fb543d25fd39`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.6-musl-x86_64.tar.gz'; 			sha256='ce413fb11de97efe8dbe4f3c57dc44741832e3a4a4187e1da590c16a4742c307'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d215968f6de73ddc81a2173017a70d9b792d5d420b9de82456b463b65e69b27`  
		Last Modified: Tue, 29 Oct 2024 22:58:54 GMT  
		Size: 179.2 MB (179208216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd06905df2b752df0007139ed460b86e49bb8bc15462444f64d11ba27bf503e7`  
		Last Modified: Tue, 29 Oct 2024 22:58:51 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-alpine` - unknown; unknown

```console
$ docker pull julia@sha256:60ddc3c77a393e45667e31f485d87245cd871e829a88fd21bfdfab7a0e58d4d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 KB (86621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0f69d006ef8e901d92b64093923dfe71d687faac73455df906537d6e605ad24`

```dockerfile
```

-	Layers:
	-	`sha256:7b26cc1e13646131ade53b6c784119a8031635ff9d41794fe7be1b5664f18c96`  
		Last Modified: Tue, 29 Oct 2024 22:58:51 GMT  
		Size: 74.2 KB (74246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0c219be1df83780b410e38a93582765d68c52f1a0642e6d68986dd3525fb867`  
		Last Modified: Tue, 29 Oct 2024 22:58:51 GMT  
		Size: 12.4 KB (12375 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-alpine3.19`

```console
$ docker pull julia@sha256:2ce80e8c54e92e67f316f91c064c8f60f25c95fc13e534611ae895dd848b972b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10-alpine3.19` - linux; amd64

```console
$ docker pull julia@sha256:faefeba9a0bf7e3b1cabc7120b2c916a3ae66078eb42ed8cfb734afe2a4fc7aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182628411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7aab12fc6ccc2a6bb60d23e3afe3ae3a7241e0c22b269aecc09aeb5fea2aa0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:13 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Fri, 06 Sep 2024 22:20:13 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.6-musl-x86_64.tar.gz'; 			sha256='ce413fb11de97efe8dbe4f3c57dc44741832e3a4a4187e1da590c16a4742c307'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9240d270085d60abcba88395eb848393ea9905668d90547b4db111720eaea7d6`  
		Last Modified: Tue, 29 Oct 2024 22:59:07 GMT  
		Size: 179.2 MB (179208337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c707901a58933ecda82b928f1d02b60d0d2c866f6ac44cf18ff1c79bcac218`  
		Last Modified: Tue, 29 Oct 2024 22:59:02 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-alpine3.19` - unknown; unknown

```console
$ docker pull julia@sha256:733865c156f0ea277e56254ed98abda76b7fa34a99fd2570f302e6dedeb72a80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 KB (89624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:326c1a4e36c3a8f8491927fb7b8be9f15aa4a47d18d9196f0b5a6f3929b59fc7`

```dockerfile
```

-	Layers:
	-	`sha256:40b461b534b703653e3d6ca3a3a1e02fb1d44266fc57869144a650340e46d3c3`  
		Last Modified: Tue, 29 Oct 2024 22:59:02 GMT  
		Size: 77.9 KB (77865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d965757f43245a227c131355c6bdf6ea1d3c905708d8d2222119d62da5f590a`  
		Last Modified: Tue, 29 Oct 2024 22:59:02 GMT  
		Size: 11.8 KB (11759 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-alpine3.20`

```console
$ docker pull julia@sha256:5f547f1d17f11ca957b3246664002aee1365ad98e7437e28ff53b33f14fa9fff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10-alpine3.20` - linux; amd64

```console
$ docker pull julia@sha256:64fd5bdc56499d4c38f939f6a40186b24cbd793cdfd0302d716bae656a0edfd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182832388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073e61618388a0ed05e82a4327440dfdbd3824aa763d09063f50fb543d25fd39`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.6-musl-x86_64.tar.gz'; 			sha256='ce413fb11de97efe8dbe4f3c57dc44741832e3a4a4187e1da590c16a4742c307'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d215968f6de73ddc81a2173017a70d9b792d5d420b9de82456b463b65e69b27`  
		Last Modified: Tue, 29 Oct 2024 22:58:54 GMT  
		Size: 179.2 MB (179208216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd06905df2b752df0007139ed460b86e49bb8bc15462444f64d11ba27bf503e7`  
		Last Modified: Tue, 29 Oct 2024 22:58:51 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-alpine3.20` - unknown; unknown

```console
$ docker pull julia@sha256:60ddc3c77a393e45667e31f485d87245cd871e829a88fd21bfdfab7a0e58d4d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 KB (86621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0f69d006ef8e901d92b64093923dfe71d687faac73455df906537d6e605ad24`

```dockerfile
```

-	Layers:
	-	`sha256:7b26cc1e13646131ade53b6c784119a8031635ff9d41794fe7be1b5664f18c96`  
		Last Modified: Tue, 29 Oct 2024 22:58:51 GMT  
		Size: 74.2 KB (74246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0c219be1df83780b410e38a93582765d68c52f1a0642e6d68986dd3525fb867`  
		Last Modified: Tue, 29 Oct 2024 22:58:51 GMT  
		Size: 12.4 KB (12375 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-bookworm`

```console
$ docker pull julia@sha256:beacce74c44411e9ff7d3a2d9c47df8da93effa5608db5513e4b80cf8f24690a
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
$ docker pull julia@sha256:066fe3c12ab811346b53168d4e6b894296b9c05c661f1160aaab7de42ba8db48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.5 MB (211469990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:650577d6aea7bd1e50734262e6250954dd8de23f0810f8e473d5b0b46ede003d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 17 Oct 2024 00:20:30 GMT
CMD ["bash"]
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.6-linux-x86_64.tar.gz'; 			sha256='8b53429e17585c66476b39f2b2279da207ea0f310c55db38f3410bdd4f6a3d49'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.6-linux-aarch64.tar.gz'; 			sha256='5530359839544ba1ee8f6f66728fd4f9b591822c1633f93cf9672c7f9528fc3a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.6-linux-i686.tar.gz'; 			sha256='52771086511905c22669bc8667a98a97ad26e82747a429165fde2641672e962b'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.6-linux-ppc64le.tar.gz'; 			sha256='bbfd63ba2bf497f82101ef8ca3e681adca4ab95f9d5e12abfb2cf3a3c72d6126'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24730e632d102308412e50d47afc4963ab80945853c21921db804fee91f70c4`  
		Last Modified: Tue, 29 Oct 2024 22:59:04 GMT  
		Size: 5.7 MB (5712693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54df6a7b1c987a3a57cf6c3a830c3d7ded854573b58fcbbc7c8ab5d975d3241b`  
		Last Modified: Tue, 29 Oct 2024 22:59:07 GMT  
		Size: 176.6 MB (176630637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f180184aba9526edbb4fa7be6a302a437d43b29f442ab8cd3062874fa38d52a1`  
		Last Modified: Tue, 29 Oct 2024 22:59:04 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:9cd8b3fc2a11d08112901e265156ad92fec39c16bd245987c402f1ecad86f33b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11687b4578ab84520d40c7e0c43a470aed5f538a5ca0b2db7132407d16805b63`

```dockerfile
```

-	Layers:
	-	`sha256:355f0872750dee81ec05047b47e309ca3afb653edcd42237934de5be5ecc1d73`  
		Last Modified: Tue, 29 Oct 2024 22:59:04 GMT  
		Size: 2.4 MB (2449212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18cccb85b4623e7a71d4bc6d3c361bc4642429b260ba99828e8b6398a6ace30e`  
		Last Modified: Tue, 29 Oct 2024 22:59:04 GMT  
		Size: 17.0 KB (17018 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:fe90cd54fa02a1a87cd43900e84872dac0e2eb6acb158a7df97cadf542412053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.0 MB (212041217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a349d4bb79aaa181d575d5c590ea369d89d19495483c28c89cc30ed9f22f9baa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.6-linux-x86_64.tar.gz'; 			sha256='8b53429e17585c66476b39f2b2279da207ea0f310c55db38f3410bdd4f6a3d49'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.6-linux-aarch64.tar.gz'; 			sha256='5530359839544ba1ee8f6f66728fd4f9b591822c1633f93cf9672c7f9528fc3a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.6-linux-i686.tar.gz'; 			sha256='52771086511905c22669bc8667a98a97ad26e82747a429165fde2641672e962b'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.6-linux-ppc64le.tar.gz'; 			sha256='bbfd63ba2bf497f82101ef8ca3e681adca4ab95f9d5e12abfb2cf3a3c72d6126'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9f7aa12a882cbec1989b7eb39edf886c46b6ec43a0dbdaa46322fb5ea3fd09`  
		Last Modified: Wed, 30 Oct 2024 00:03:43 GMT  
		Size: 5.5 MB (5537174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba2ee9345c139face9d10e01386b6012aa72822b7e356753ae9c5a875667fad`  
		Last Modified: Wed, 30 Oct 2024 00:03:47 GMT  
		Size: 177.3 MB (177347335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1623697d698db51239d0786367179ae5b9fdda3d9646d150726d51f4d05911`  
		Last Modified: Wed, 30 Oct 2024 00:03:42 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:0713eadec1bcf05f96c35d1be3349adfdba8398cd7e7141c0c397678f7199e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ef0d98ccdd9762f43506d01f867a1a6b49cbf1c69f3de0971422f25f8d61d5`

```dockerfile
```

-	Layers:
	-	`sha256:301ab6e57c61cb7bbd0857cd1cdc41631539edf83c6f8ed5e2116b5121b95800`  
		Last Modified: Wed, 30 Oct 2024 00:03:43 GMT  
		Size: 2.4 MB (2448264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:263e7cad0f4326e8b1f9b2a1bf2ad5ca2de932f3be76f4fcc153bbfeb6859c5b`  
		Last Modified: Wed, 30 Oct 2024 00:03:42 GMT  
		Size: 17.2 KB (17155 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; 386

```console
$ docker pull julia@sha256:c718d318da6995a7c5ed037813139bc5475763c90c69462b23a9c13f264071f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193827906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:142e4513d0ab21eb84ec458e70e790a6739e3398c6b63e4d2f7cf015259c8c9e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 17 Oct 2024 00:38:56 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Thu, 17 Oct 2024 00:38:56 GMT
CMD ["bash"]
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.6-linux-x86_64.tar.gz'; 			sha256='8b53429e17585c66476b39f2b2279da207ea0f310c55db38f3410bdd4f6a3d49'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.6-linux-aarch64.tar.gz'; 			sha256='5530359839544ba1ee8f6f66728fd4f9b591822c1633f93cf9672c7f9528fc3a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.6-linux-i686.tar.gz'; 			sha256='52771086511905c22669bc8667a98a97ad26e82747a429165fde2641672e962b'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.6-linux-ppc64le.tar.gz'; 			sha256='bbfd63ba2bf497f82101ef8ca3e681adca4ab95f9d5e12abfb2cf3a3c72d6126'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c544b64767c8ee9ec5202884260726a080b68fa738ff648f1936b53eb005db63`  
		Last Modified: Tue, 29 Oct 2024 22:59:02 GMT  
		Size: 5.9 MB (5870458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714cab6622ab2b57035ee3dbf90756fcc815ac79da12048a7416501899f30f15`  
		Last Modified: Tue, 29 Oct 2024 22:59:06 GMT  
		Size: 157.8 MB (157812811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135081bef526546ebd94b2b8c30a901dba8d23fb0d246f7784beecc4bcb2bf10`  
		Last Modified: Tue, 29 Oct 2024 22:59:02 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:bf6a8c8863c5670bf815c39bba3a0187df9dd2d04b885d1763f55fd9a169b1c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e27864b80a3b3c70874b2e512ecb8d105dc0ee3197d0e994acc19c4a3fbdc6e`

```dockerfile
```

-	Layers:
	-	`sha256:ec727e80c071bab5a789d0f27b0127857ca592daba008e3c2624602ffa12a9ed`  
		Last Modified: Tue, 29 Oct 2024 22:59:02 GMT  
		Size: 2.4 MB (2446304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8b8b1cbd3886057906d657ef37a305a39bc310e1a3cc8a9087fe2df9138a512`  
		Last Modified: Tue, 29 Oct 2024 22:59:02 GMT  
		Size: 17.0 KB (17011 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:c4c48e226ac08b9e19836392b0979936d62b3d7a36e84c5360d1d1b2b2d81547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.7 MB (194677985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17067b8f17bce468e0c9eeb8dc4f3ec6582dc539140ec4f27e41d606949f8b0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 17 Oct 2024 01:18:54 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Thu, 17 Oct 2024 01:18:56 GMT
CMD ["bash"]
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.6-linux-x86_64.tar.gz'; 			sha256='8b53429e17585c66476b39f2b2279da207ea0f310c55db38f3410bdd4f6a3d49'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.6-linux-aarch64.tar.gz'; 			sha256='5530359839544ba1ee8f6f66728fd4f9b591822c1633f93cf9672c7f9528fc3a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.6-linux-i686.tar.gz'; 			sha256='52771086511905c22669bc8667a98a97ad26e82747a429165fde2641672e962b'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.6-linux-ppc64le.tar.gz'; 			sha256='bbfd63ba2bf497f82101ef8ca3e681adca4ab95f9d5e12abfb2cf3a3c72d6126'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872ce7d06e1f062f97505b0e301bbfdbf0eb9be16d7514467915e735ab53c113`  
		Last Modified: Tue, 29 Oct 2024 23:01:05 GMT  
		Size: 6.2 MB (6247957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170dcc05149f98f3db1198fddc1be23f82b6ae0fcf50dd96e047466a8af395ac`  
		Last Modified: Tue, 29 Oct 2024 23:01:09 GMT  
		Size: 155.3 MB (155307456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbf0fac49cd21372305ab812b69a2b403d1f62371f492ce96e9f307669893dc`  
		Last Modified: Tue, 29 Oct 2024 23:01:04 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:605795e6f38be17a1fcaa2cfe024c183d09af212ccb061fa4ad2cf2d6b71b471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2469479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c724732b12d6ed77c9b813e7f50d05a34b89ea234bc8ceefbf789e5cf2ebcef0`

```dockerfile
```

-	Layers:
	-	`sha256:6f53f1adeb9f8fbab7623a47e3466557398985eb384c51887fbdfa6f9c1ca791`  
		Last Modified: Tue, 29 Oct 2024 23:01:05 GMT  
		Size: 2.5 MB (2452397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb684095369776335de241209d640d5a1f006b954d8abead862abffbbe157cf2`  
		Last Modified: Tue, 29 Oct 2024 23:01:04 GMT  
		Size: 17.1 KB (17082 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-bullseye`

```console
$ docker pull julia@sha256:d9ed59097266c0abd5e00d57846e361d1854cf794738e53579e5cb4bf23507a4
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
$ docker pull julia@sha256:602199cc58de0e1f59848914cf84dee71a95eb212f6bad22fb75f5bc7ff1209a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.5 MB (210486630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6d163780e512dddadcb37f8647b74edd2f24e40c9c954067c0dacd97cda6de0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:51 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
# Thu, 17 Oct 2024 00:20:52 GMT
CMD ["bash"]
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.6-linux-x86_64.tar.gz'; 			sha256='8b53429e17585c66476b39f2b2279da207ea0f310c55db38f3410bdd4f6a3d49'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.6-linux-aarch64.tar.gz'; 			sha256='5530359839544ba1ee8f6f66728fd4f9b591822c1633f93cf9672c7f9528fc3a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.6-linux-i686.tar.gz'; 			sha256='52771086511905c22669bc8667a98a97ad26e82747a429165fde2641672e962b'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.6-linux-ppc64le.tar.gz'; 			sha256='bbfd63ba2bf497f82101ef8ca3e681adca4ab95f9d5e12abfb2cf3a3c72d6126'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24b711ff7d16b77620f37463d5955fdffc6028b0c517834f3e2b44c13f1acde`  
		Last Modified: Tue, 29 Oct 2024 22:59:07 GMT  
		Size: 2.4 MB (2426561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca054cf855c07696a5cbceb538284ec5b871d967630cba2def7b697f0b8bb0fc`  
		Last Modified: Tue, 29 Oct 2024 22:59:10 GMT  
		Size: 176.6 MB (176630899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc80302bd481b1a67cec4e3009fa2d64c00c75313b48ba2d4536cdc3b9d396e`  
		Last Modified: Tue, 29 Oct 2024 22:59:07 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:298558b1d8b65dda22bf1e4f926ca59476fe21167dfd3fc1c5ba4b0484e11135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2734071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef18ec26fa0f2ed57e23dde9b6b0b86dda90853dff90b16c917c2061f98b3ba4`

```dockerfile
```

-	Layers:
	-	`sha256:49e39ae4e4090a91039a769e05f8b2d38bb8cb63c7b0a21573d3250d35641360`  
		Last Modified: Tue, 29 Oct 2024 22:59:07 GMT  
		Size: 2.7 MB (2717617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bd8319123f41f50b738b9bea9adfe950ac5c7911904ab6619c6da965daaa5bf`  
		Last Modified: Tue, 29 Oct 2024 22:59:07 GMT  
		Size: 16.5 KB (16454 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:5a0ed26284ea162ba042b10cd0657cef6ed1ee8e33543f3b6eba58afa119ad1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.8 MB (209838984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:582f2f475e880b9f25ddc1ca8170a2947fb5ba3978b3446fb800fc65bb632c86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:13 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Thu, 17 Oct 2024 01:12:14 GMT
CMD ["bash"]
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.6-linux-x86_64.tar.gz'; 			sha256='8b53429e17585c66476b39f2b2279da207ea0f310c55db38f3410bdd4f6a3d49'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.6-linux-aarch64.tar.gz'; 			sha256='5530359839544ba1ee8f6f66728fd4f9b591822c1633f93cf9672c7f9528fc3a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.6-linux-i686.tar.gz'; 			sha256='52771086511905c22669bc8667a98a97ad26e82747a429165fde2641672e962b'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.6-linux-ppc64le.tar.gz'; 			sha256='bbfd63ba2bf497f82101ef8ca3e681adca4ab95f9d5e12abfb2cf3a3c72d6126'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8def44bdef5469eb29a86fa0a8c5904a811f78e825d26e28e2867f1953b48b20`  
		Last Modified: Wed, 30 Oct 2024 00:04:57 GMT  
		Size: 2.4 MB (2415135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce676b526ca999e66c3b1e1fc051b7f8626b6f595834e4ea894e43f4fd7d77cf`  
		Last Modified: Wed, 30 Oct 2024 00:05:01 GMT  
		Size: 177.3 MB (177347721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab419172de04012ccd11c2b4cd457b75f9ae0833fb6052fd9b05e054238f8be`  
		Last Modified: Wed, 30 Oct 2024 00:04:56 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:2b3acb7550a4e64071aad1e929ce4b0c9d2dc4401f51d20159eba52ed5053dc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2733175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e838849e3ac3a25a3ad3af62b27bb199edcd0960452ce74e1eaeaa99fc0789`

```dockerfile
```

-	Layers:
	-	`sha256:a390bb685be997573cafbe327619e268421efe9068c6882c47203144cf781b6e`  
		Last Modified: Wed, 30 Oct 2024 00:04:57 GMT  
		Size: 2.7 MB (2716633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a20066a10e7d7f68f92879db8ef288b03041321c70d57e582d7f9335987d68c`  
		Last Modified: Wed, 30 Oct 2024 00:04:56 GMT  
		Size: 16.5 KB (16542 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bullseye` - linux; 386

```console
$ docker pull julia@sha256:075542375efbdea852b4788a73ace5bbc6f46ce67bb4533671810239458265c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192760616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96da4367a97ec41859b8598c03f0d979467b238c6d1d2b49f6a548b4c0f465bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 17 Oct 2024 00:39:19 GMT
ADD file:05098c6b0b4cfde8b4ffadc861fc7668bbf1779983d50b6be61989e6378fc17b in / 
# Thu, 17 Oct 2024 00:39:20 GMT
CMD ["bash"]
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.6-linux-x86_64.tar.gz'; 			sha256='8b53429e17585c66476b39f2b2279da207ea0f310c55db38f3410bdd4f6a3d49'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.6-linux-aarch64.tar.gz'; 			sha256='5530359839544ba1ee8f6f66728fd4f9b591822c1633f93cf9672c7f9528fc3a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.6-linux-i686.tar.gz'; 			sha256='52771086511905c22669bc8667a98a97ad26e82747a429165fde2641672e962b'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.6-linux-ppc64le.tar.gz'; 			sha256='bbfd63ba2bf497f82101ef8ca3e681adca4ab95f9d5e12abfb2cf3a3c72d6126'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0aff79075c186716daeb376e46e89131aa14f0dc2bd8f794bd04d72494cb4693`  
		Last Modified: Thu, 17 Oct 2024 00:43:15 GMT  
		Size: 32.4 MB (32413830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf8ae6599e3b396cdad1e37cf3e67a4baf9ec59452708eb157c5da6df26ddec`  
		Last Modified: Tue, 29 Oct 2024 22:59:08 GMT  
		Size: 2.5 MB (2532988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6781032aff8d458d7f5fd30b797d1936118b305311e91866d98bf9fc04f80150`  
		Last Modified: Tue, 29 Oct 2024 22:59:12 GMT  
		Size: 157.8 MB (157813426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55877412772a1d62133cc585994847d91e3d4d4de2dec59b22698fcf197604c6`  
		Last Modified: Tue, 29 Oct 2024 22:59:08 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:2ab9c04ae6075411f3f8d0a1cf4ef4b5329b3c26138be2bd3150ab271abaaacb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2731158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5eafa68ad6a8e6437cc4fd6d7d3f28709342c2c4f8b91676592155ceda6da40`

```dockerfile
```

-	Layers:
	-	`sha256:be884603289a6063f8bbf2088dc94bb247d9563e716c8dcb2daeb1c18f2ead3e`  
		Last Modified: Tue, 29 Oct 2024 22:59:08 GMT  
		Size: 2.7 MB (2714725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80537ad0f08f28d9da4c02ce1cdd8d65a25e1be1ecf1972c314b506724b3a7b5`  
		Last Modified: Tue, 29 Oct 2024 22:59:08 GMT  
		Size: 16.4 KB (16433 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-windowsservercore`

```console
$ docker pull julia@sha256:bad5fd470043108972fab03ab7fba19dd1a37e13481871a96cfaccc0c9a78304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `julia:1.10-windowsservercore` - windows version 10.0.20348.2762; amd64

```console
$ docker pull julia@sha256:0e742f15776e4f7e2466446691d4e7d0ae81576fea07e6ac69eea39d103d0173
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1988310186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3085046212c05c9e4b0a731e38e30128a7ac793956c2995e4417d66e1888e4b8`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Tue, 29 Oct 2024 23:56:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 29 Oct 2024 23:56:59 GMT
ENV JULIA_VERSION=1.10.6
# Tue, 29 Oct 2024 23:57:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.6-win64.exe
# Tue, 29 Oct 2024 23:57:02 GMT
ENV JULIA_SHA256=f29e62ea3edede6b9a245ca1117d5f5232a78f324902a69368e3ed5836f96d59
# Tue, 29 Oct 2024 23:59:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 29 Oct 2024 23:59:25 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a703ec8db6afe2491ab0518ad479df3ea9eb52d5967771bcebf035a59b29d6`  
		Last Modified: Tue, 29 Oct 2024 23:59:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8738f7e52db049fd38af00a87bd6e9119f5abbd70ab1bd552a1f01f9785c6b5d`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0083b70e021328f6ae7e9d213e77735279f1cf457c243584e8cea8bad89d18`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220778260973a205a267336a441e793360c94d727e8fce10de071e7edb0fa48b`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc4ea8989979e5b3bdf5bafb635c0dd5f91c792a52a23c77f353466f2dbeea3`  
		Last Modified: Tue, 29 Oct 2024 23:59:50 GMT  
		Size: 189.0 MB (188962205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ae0a51fc94fd2d69da5be3323e71e7737e28dd291e65c140e1836658098af0`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10-windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull julia@sha256:6ca14732d9b63fca4b7397eadd040a3c87ccd84e1ba749fb7e1ee9bc42244913
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2090791615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d349843745bd27b77509eb661965f36217fa3b818dd96f5ef8ad5d5c868c8d93`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 29 Oct 2024 22:58:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 29 Oct 2024 22:58:31 GMT
ENV JULIA_VERSION=1.10.6
# Tue, 29 Oct 2024 22:58:32 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.6-win64.exe
# Tue, 29 Oct 2024 22:58:33 GMT
ENV JULIA_SHA256=f29e62ea3edede6b9a245ca1117d5f5232a78f324902a69368e3ed5836f96d59
# Tue, 29 Oct 2024 23:00:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 29 Oct 2024 23:00:38 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187f98b1f55258e314fedb9c2f6226e1c2a11740febbd0ce89d238e43c0bed2`  
		Last Modified: Tue, 29 Oct 2024 23:00:43 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba0606836b66ce8f497eac48f690ee807b532d6777b4e56ce704dd15e77e678a`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9b820753126ccfc32f3fba865e5d5b4824aedcdaf3831831d2844d43d919f6`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0726905f5fbf316e8c8c6741bc1793dde3958dca4f53a28ff39972d4253b31`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88eff14262dc220189629e33a16987149944ad23b1b5f939113fa634c51f7f4b`  
		Last Modified: Tue, 29 Oct 2024 23:01:04 GMT  
		Size: 189.0 MB (188959879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a37e9e4b5cd836f0416d006af1817bf06ea1be011782932bf2b3785e6a08c44`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-windowsservercore-1809`

```console
$ docker pull julia@sha256:58087ae2d9648fa6b36d657e915e543117eeae1bb7dd7ecd19ab015510e67d32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `julia:1.10-windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull julia@sha256:6ca14732d9b63fca4b7397eadd040a3c87ccd84e1ba749fb7e1ee9bc42244913
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2090791615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d349843745bd27b77509eb661965f36217fa3b818dd96f5ef8ad5d5c868c8d93`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 29 Oct 2024 22:58:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 29 Oct 2024 22:58:31 GMT
ENV JULIA_VERSION=1.10.6
# Tue, 29 Oct 2024 22:58:32 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.6-win64.exe
# Tue, 29 Oct 2024 22:58:33 GMT
ENV JULIA_SHA256=f29e62ea3edede6b9a245ca1117d5f5232a78f324902a69368e3ed5836f96d59
# Tue, 29 Oct 2024 23:00:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 29 Oct 2024 23:00:38 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187f98b1f55258e314fedb9c2f6226e1c2a11740febbd0ce89d238e43c0bed2`  
		Last Modified: Tue, 29 Oct 2024 23:00:43 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba0606836b66ce8f497eac48f690ee807b532d6777b4e56ce704dd15e77e678a`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9b820753126ccfc32f3fba865e5d5b4824aedcdaf3831831d2844d43d919f6`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0726905f5fbf316e8c8c6741bc1793dde3958dca4f53a28ff39972d4253b31`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88eff14262dc220189629e33a16987149944ad23b1b5f939113fa634c51f7f4b`  
		Last Modified: Tue, 29 Oct 2024 23:01:04 GMT  
		Size: 189.0 MB (188959879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a37e9e4b5cd836f0416d006af1817bf06ea1be011782932bf2b3785e6a08c44`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:0e65c00e6c1db3fd045c6a7adc21172ef95b4163656cc090fe6155b59939459c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `julia:1.10-windowsservercore-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull julia@sha256:0e742f15776e4f7e2466446691d4e7d0ae81576fea07e6ac69eea39d103d0173
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1988310186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3085046212c05c9e4b0a731e38e30128a7ac793956c2995e4417d66e1888e4b8`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Tue, 29 Oct 2024 23:56:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 29 Oct 2024 23:56:59 GMT
ENV JULIA_VERSION=1.10.6
# Tue, 29 Oct 2024 23:57:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.6-win64.exe
# Tue, 29 Oct 2024 23:57:02 GMT
ENV JULIA_SHA256=f29e62ea3edede6b9a245ca1117d5f5232a78f324902a69368e3ed5836f96d59
# Tue, 29 Oct 2024 23:59:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 29 Oct 2024 23:59:25 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a703ec8db6afe2491ab0518ad479df3ea9eb52d5967771bcebf035a59b29d6`  
		Last Modified: Tue, 29 Oct 2024 23:59:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8738f7e52db049fd38af00a87bd6e9119f5abbd70ab1bd552a1f01f9785c6b5d`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0083b70e021328f6ae7e9d213e77735279f1cf457c243584e8cea8bad89d18`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220778260973a205a267336a441e793360c94d727e8fce10de071e7edb0fa48b`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc4ea8989979e5b3bdf5bafb635c0dd5f91c792a52a23c77f353466f2dbeea3`  
		Last Modified: Tue, 29 Oct 2024 23:59:50 GMT  
		Size: 189.0 MB (188962205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ae0a51fc94fd2d69da5be3323e71e7737e28dd291e65c140e1836658098af0`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.6`

```console
$ docker pull julia@sha256:2e8a399601c766e397f9afdccb23dce25240605c48e59657947af3cfa3b80118
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
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `julia:1.10.6` - linux; amd64

```console
$ docker pull julia@sha256:066fe3c12ab811346b53168d4e6b894296b9c05c661f1160aaab7de42ba8db48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.5 MB (211469990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:650577d6aea7bd1e50734262e6250954dd8de23f0810f8e473d5b0b46ede003d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 17 Oct 2024 00:20:30 GMT
CMD ["bash"]
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.6-linux-x86_64.tar.gz'; 			sha256='8b53429e17585c66476b39f2b2279da207ea0f310c55db38f3410bdd4f6a3d49'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.6-linux-aarch64.tar.gz'; 			sha256='5530359839544ba1ee8f6f66728fd4f9b591822c1633f93cf9672c7f9528fc3a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.6-linux-i686.tar.gz'; 			sha256='52771086511905c22669bc8667a98a97ad26e82747a429165fde2641672e962b'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.6-linux-ppc64le.tar.gz'; 			sha256='bbfd63ba2bf497f82101ef8ca3e681adca4ab95f9d5e12abfb2cf3a3c72d6126'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24730e632d102308412e50d47afc4963ab80945853c21921db804fee91f70c4`  
		Last Modified: Tue, 29 Oct 2024 22:59:04 GMT  
		Size: 5.7 MB (5712693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54df6a7b1c987a3a57cf6c3a830c3d7ded854573b58fcbbc7c8ab5d975d3241b`  
		Last Modified: Tue, 29 Oct 2024 22:59:07 GMT  
		Size: 176.6 MB (176630637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f180184aba9526edbb4fa7be6a302a437d43b29f442ab8cd3062874fa38d52a1`  
		Last Modified: Tue, 29 Oct 2024 22:59:04 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.6` - unknown; unknown

```console
$ docker pull julia@sha256:9cd8b3fc2a11d08112901e265156ad92fec39c16bd245987c402f1ecad86f33b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11687b4578ab84520d40c7e0c43a470aed5f538a5ca0b2db7132407d16805b63`

```dockerfile
```

-	Layers:
	-	`sha256:355f0872750dee81ec05047b47e309ca3afb653edcd42237934de5be5ecc1d73`  
		Last Modified: Tue, 29 Oct 2024 22:59:04 GMT  
		Size: 2.4 MB (2449212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18cccb85b4623e7a71d4bc6d3c361bc4642429b260ba99828e8b6398a6ace30e`  
		Last Modified: Tue, 29 Oct 2024 22:59:04 GMT  
		Size: 17.0 KB (17018 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.6` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:fe90cd54fa02a1a87cd43900e84872dac0e2eb6acb158a7df97cadf542412053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.0 MB (212041217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a349d4bb79aaa181d575d5c590ea369d89d19495483c28c89cc30ed9f22f9baa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.6-linux-x86_64.tar.gz'; 			sha256='8b53429e17585c66476b39f2b2279da207ea0f310c55db38f3410bdd4f6a3d49'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.6-linux-aarch64.tar.gz'; 			sha256='5530359839544ba1ee8f6f66728fd4f9b591822c1633f93cf9672c7f9528fc3a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.6-linux-i686.tar.gz'; 			sha256='52771086511905c22669bc8667a98a97ad26e82747a429165fde2641672e962b'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.6-linux-ppc64le.tar.gz'; 			sha256='bbfd63ba2bf497f82101ef8ca3e681adca4ab95f9d5e12abfb2cf3a3c72d6126'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9f7aa12a882cbec1989b7eb39edf886c46b6ec43a0dbdaa46322fb5ea3fd09`  
		Last Modified: Wed, 30 Oct 2024 00:03:43 GMT  
		Size: 5.5 MB (5537174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba2ee9345c139face9d10e01386b6012aa72822b7e356753ae9c5a875667fad`  
		Last Modified: Wed, 30 Oct 2024 00:03:47 GMT  
		Size: 177.3 MB (177347335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1623697d698db51239d0786367179ae5b9fdda3d9646d150726d51f4d05911`  
		Last Modified: Wed, 30 Oct 2024 00:03:42 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.6` - unknown; unknown

```console
$ docker pull julia@sha256:0713eadec1bcf05f96c35d1be3349adfdba8398cd7e7141c0c397678f7199e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ef0d98ccdd9762f43506d01f867a1a6b49cbf1c69f3de0971422f25f8d61d5`

```dockerfile
```

-	Layers:
	-	`sha256:301ab6e57c61cb7bbd0857cd1cdc41631539edf83c6f8ed5e2116b5121b95800`  
		Last Modified: Wed, 30 Oct 2024 00:03:43 GMT  
		Size: 2.4 MB (2448264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:263e7cad0f4326e8b1f9b2a1bf2ad5ca2de932f3be76f4fcc153bbfeb6859c5b`  
		Last Modified: Wed, 30 Oct 2024 00:03:42 GMT  
		Size: 17.2 KB (17155 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.6` - linux; 386

```console
$ docker pull julia@sha256:c718d318da6995a7c5ed037813139bc5475763c90c69462b23a9c13f264071f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193827906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:142e4513d0ab21eb84ec458e70e790a6739e3398c6b63e4d2f7cf015259c8c9e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 17 Oct 2024 00:38:56 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Thu, 17 Oct 2024 00:38:56 GMT
CMD ["bash"]
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.6-linux-x86_64.tar.gz'; 			sha256='8b53429e17585c66476b39f2b2279da207ea0f310c55db38f3410bdd4f6a3d49'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.6-linux-aarch64.tar.gz'; 			sha256='5530359839544ba1ee8f6f66728fd4f9b591822c1633f93cf9672c7f9528fc3a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.6-linux-i686.tar.gz'; 			sha256='52771086511905c22669bc8667a98a97ad26e82747a429165fde2641672e962b'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.6-linux-ppc64le.tar.gz'; 			sha256='bbfd63ba2bf497f82101ef8ca3e681adca4ab95f9d5e12abfb2cf3a3c72d6126'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c544b64767c8ee9ec5202884260726a080b68fa738ff648f1936b53eb005db63`  
		Last Modified: Tue, 29 Oct 2024 22:59:02 GMT  
		Size: 5.9 MB (5870458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714cab6622ab2b57035ee3dbf90756fcc815ac79da12048a7416501899f30f15`  
		Last Modified: Tue, 29 Oct 2024 22:59:06 GMT  
		Size: 157.8 MB (157812811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135081bef526546ebd94b2b8c30a901dba8d23fb0d246f7784beecc4bcb2bf10`  
		Last Modified: Tue, 29 Oct 2024 22:59:02 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.6` - unknown; unknown

```console
$ docker pull julia@sha256:bf6a8c8863c5670bf815c39bba3a0187df9dd2d04b885d1763f55fd9a169b1c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e27864b80a3b3c70874b2e512ecb8d105dc0ee3197d0e994acc19c4a3fbdc6e`

```dockerfile
```

-	Layers:
	-	`sha256:ec727e80c071bab5a789d0f27b0127857ca592daba008e3c2624602ffa12a9ed`  
		Last Modified: Tue, 29 Oct 2024 22:59:02 GMT  
		Size: 2.4 MB (2446304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8b8b1cbd3886057906d657ef37a305a39bc310e1a3cc8a9087fe2df9138a512`  
		Last Modified: Tue, 29 Oct 2024 22:59:02 GMT  
		Size: 17.0 KB (17011 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.6` - linux; ppc64le

```console
$ docker pull julia@sha256:c4c48e226ac08b9e19836392b0979936d62b3d7a36e84c5360d1d1b2b2d81547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.7 MB (194677985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17067b8f17bce468e0c9eeb8dc4f3ec6582dc539140ec4f27e41d606949f8b0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 17 Oct 2024 01:18:54 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Thu, 17 Oct 2024 01:18:56 GMT
CMD ["bash"]
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.6-linux-x86_64.tar.gz'; 			sha256='8b53429e17585c66476b39f2b2279da207ea0f310c55db38f3410bdd4f6a3d49'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.6-linux-aarch64.tar.gz'; 			sha256='5530359839544ba1ee8f6f66728fd4f9b591822c1633f93cf9672c7f9528fc3a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.6-linux-i686.tar.gz'; 			sha256='52771086511905c22669bc8667a98a97ad26e82747a429165fde2641672e962b'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.6-linux-ppc64le.tar.gz'; 			sha256='bbfd63ba2bf497f82101ef8ca3e681adca4ab95f9d5e12abfb2cf3a3c72d6126'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872ce7d06e1f062f97505b0e301bbfdbf0eb9be16d7514467915e735ab53c113`  
		Last Modified: Tue, 29 Oct 2024 23:01:05 GMT  
		Size: 6.2 MB (6247957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170dcc05149f98f3db1198fddc1be23f82b6ae0fcf50dd96e047466a8af395ac`  
		Last Modified: Tue, 29 Oct 2024 23:01:09 GMT  
		Size: 155.3 MB (155307456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbf0fac49cd21372305ab812b69a2b403d1f62371f492ce96e9f307669893dc`  
		Last Modified: Tue, 29 Oct 2024 23:01:04 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.6` - unknown; unknown

```console
$ docker pull julia@sha256:605795e6f38be17a1fcaa2cfe024c183d09af212ccb061fa4ad2cf2d6b71b471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2469479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c724732b12d6ed77c9b813e7f50d05a34b89ea234bc8ceefbf789e5cf2ebcef0`

```dockerfile
```

-	Layers:
	-	`sha256:6f53f1adeb9f8fbab7623a47e3466557398985eb384c51887fbdfa6f9c1ca791`  
		Last Modified: Tue, 29 Oct 2024 23:01:05 GMT  
		Size: 2.5 MB (2452397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb684095369776335de241209d640d5a1f006b954d8abead862abffbbe157cf2`  
		Last Modified: Tue, 29 Oct 2024 23:01:04 GMT  
		Size: 17.1 KB (17082 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.6` - windows version 10.0.20348.2762; amd64

```console
$ docker pull julia@sha256:0e742f15776e4f7e2466446691d4e7d0ae81576fea07e6ac69eea39d103d0173
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1988310186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3085046212c05c9e4b0a731e38e30128a7ac793956c2995e4417d66e1888e4b8`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Tue, 29 Oct 2024 23:56:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 29 Oct 2024 23:56:59 GMT
ENV JULIA_VERSION=1.10.6
# Tue, 29 Oct 2024 23:57:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.6-win64.exe
# Tue, 29 Oct 2024 23:57:02 GMT
ENV JULIA_SHA256=f29e62ea3edede6b9a245ca1117d5f5232a78f324902a69368e3ed5836f96d59
# Tue, 29 Oct 2024 23:59:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 29 Oct 2024 23:59:25 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a703ec8db6afe2491ab0518ad479df3ea9eb52d5967771bcebf035a59b29d6`  
		Last Modified: Tue, 29 Oct 2024 23:59:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8738f7e52db049fd38af00a87bd6e9119f5abbd70ab1bd552a1f01f9785c6b5d`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0083b70e021328f6ae7e9d213e77735279f1cf457c243584e8cea8bad89d18`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220778260973a205a267336a441e793360c94d727e8fce10de071e7edb0fa48b`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc4ea8989979e5b3bdf5bafb635c0dd5f91c792a52a23c77f353466f2dbeea3`  
		Last Modified: Tue, 29 Oct 2024 23:59:50 GMT  
		Size: 189.0 MB (188962205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ae0a51fc94fd2d69da5be3323e71e7737e28dd291e65c140e1836658098af0`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10.6` - windows version 10.0.17763.6414; amd64

```console
$ docker pull julia@sha256:6ca14732d9b63fca4b7397eadd040a3c87ccd84e1ba749fb7e1ee9bc42244913
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2090791615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d349843745bd27b77509eb661965f36217fa3b818dd96f5ef8ad5d5c868c8d93`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 29 Oct 2024 22:58:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 29 Oct 2024 22:58:31 GMT
ENV JULIA_VERSION=1.10.6
# Tue, 29 Oct 2024 22:58:32 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.6-win64.exe
# Tue, 29 Oct 2024 22:58:33 GMT
ENV JULIA_SHA256=f29e62ea3edede6b9a245ca1117d5f5232a78f324902a69368e3ed5836f96d59
# Tue, 29 Oct 2024 23:00:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 29 Oct 2024 23:00:38 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187f98b1f55258e314fedb9c2f6226e1c2a11740febbd0ce89d238e43c0bed2`  
		Last Modified: Tue, 29 Oct 2024 23:00:43 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba0606836b66ce8f497eac48f690ee807b532d6777b4e56ce704dd15e77e678a`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9b820753126ccfc32f3fba865e5d5b4824aedcdaf3831831d2844d43d919f6`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0726905f5fbf316e8c8c6741bc1793dde3958dca4f53a28ff39972d4253b31`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88eff14262dc220189629e33a16987149944ad23b1b5f939113fa634c51f7f4b`  
		Last Modified: Tue, 29 Oct 2024 23:01:04 GMT  
		Size: 189.0 MB (188959879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a37e9e4b5cd836f0416d006af1817bf06ea1be011782932bf2b3785e6a08c44`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.6-alpine`

```console
$ docker pull julia@sha256:5f547f1d17f11ca957b3246664002aee1365ad98e7437e28ff53b33f14fa9fff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10.6-alpine` - linux; amd64

```console
$ docker pull julia@sha256:64fd5bdc56499d4c38f939f6a40186b24cbd793cdfd0302d716bae656a0edfd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182832388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073e61618388a0ed05e82a4327440dfdbd3824aa763d09063f50fb543d25fd39`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.6-musl-x86_64.tar.gz'; 			sha256='ce413fb11de97efe8dbe4f3c57dc44741832e3a4a4187e1da590c16a4742c307'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d215968f6de73ddc81a2173017a70d9b792d5d420b9de82456b463b65e69b27`  
		Last Modified: Tue, 29 Oct 2024 22:58:54 GMT  
		Size: 179.2 MB (179208216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd06905df2b752df0007139ed460b86e49bb8bc15462444f64d11ba27bf503e7`  
		Last Modified: Tue, 29 Oct 2024 22:58:51 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.6-alpine` - unknown; unknown

```console
$ docker pull julia@sha256:60ddc3c77a393e45667e31f485d87245cd871e829a88fd21bfdfab7a0e58d4d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 KB (86621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0f69d006ef8e901d92b64093923dfe71d687faac73455df906537d6e605ad24`

```dockerfile
```

-	Layers:
	-	`sha256:7b26cc1e13646131ade53b6c784119a8031635ff9d41794fe7be1b5664f18c96`  
		Last Modified: Tue, 29 Oct 2024 22:58:51 GMT  
		Size: 74.2 KB (74246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0c219be1df83780b410e38a93582765d68c52f1a0642e6d68986dd3525fb867`  
		Last Modified: Tue, 29 Oct 2024 22:58:51 GMT  
		Size: 12.4 KB (12375 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.6-alpine3.19`

```console
$ docker pull julia@sha256:2ce80e8c54e92e67f316f91c064c8f60f25c95fc13e534611ae895dd848b972b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10.6-alpine3.19` - linux; amd64

```console
$ docker pull julia@sha256:faefeba9a0bf7e3b1cabc7120b2c916a3ae66078eb42ed8cfb734afe2a4fc7aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182628411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7aab12fc6ccc2a6bb60d23e3afe3ae3a7241e0c22b269aecc09aeb5fea2aa0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:13 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Fri, 06 Sep 2024 22:20:13 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.6-musl-x86_64.tar.gz'; 			sha256='ce413fb11de97efe8dbe4f3c57dc44741832e3a4a4187e1da590c16a4742c307'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9240d270085d60abcba88395eb848393ea9905668d90547b4db111720eaea7d6`  
		Last Modified: Tue, 29 Oct 2024 22:59:07 GMT  
		Size: 179.2 MB (179208337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c707901a58933ecda82b928f1d02b60d0d2c866f6ac44cf18ff1c79bcac218`  
		Last Modified: Tue, 29 Oct 2024 22:59:02 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.6-alpine3.19` - unknown; unknown

```console
$ docker pull julia@sha256:733865c156f0ea277e56254ed98abda76b7fa34a99fd2570f302e6dedeb72a80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 KB (89624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:326c1a4e36c3a8f8491927fb7b8be9f15aa4a47d18d9196f0b5a6f3929b59fc7`

```dockerfile
```

-	Layers:
	-	`sha256:40b461b534b703653e3d6ca3a3a1e02fb1d44266fc57869144a650340e46d3c3`  
		Last Modified: Tue, 29 Oct 2024 22:59:02 GMT  
		Size: 77.9 KB (77865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d965757f43245a227c131355c6bdf6ea1d3c905708d8d2222119d62da5f590a`  
		Last Modified: Tue, 29 Oct 2024 22:59:02 GMT  
		Size: 11.8 KB (11759 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.6-alpine3.20`

```console
$ docker pull julia@sha256:5f547f1d17f11ca957b3246664002aee1365ad98e7437e28ff53b33f14fa9fff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10.6-alpine3.20` - linux; amd64

```console
$ docker pull julia@sha256:64fd5bdc56499d4c38f939f6a40186b24cbd793cdfd0302d716bae656a0edfd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182832388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073e61618388a0ed05e82a4327440dfdbd3824aa763d09063f50fb543d25fd39`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.6-musl-x86_64.tar.gz'; 			sha256='ce413fb11de97efe8dbe4f3c57dc44741832e3a4a4187e1da590c16a4742c307'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d215968f6de73ddc81a2173017a70d9b792d5d420b9de82456b463b65e69b27`  
		Last Modified: Tue, 29 Oct 2024 22:58:54 GMT  
		Size: 179.2 MB (179208216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd06905df2b752df0007139ed460b86e49bb8bc15462444f64d11ba27bf503e7`  
		Last Modified: Tue, 29 Oct 2024 22:58:51 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.6-alpine3.20` - unknown; unknown

```console
$ docker pull julia@sha256:60ddc3c77a393e45667e31f485d87245cd871e829a88fd21bfdfab7a0e58d4d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 KB (86621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0f69d006ef8e901d92b64093923dfe71d687faac73455df906537d6e605ad24`

```dockerfile
```

-	Layers:
	-	`sha256:7b26cc1e13646131ade53b6c784119a8031635ff9d41794fe7be1b5664f18c96`  
		Last Modified: Tue, 29 Oct 2024 22:58:51 GMT  
		Size: 74.2 KB (74246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0c219be1df83780b410e38a93582765d68c52f1a0642e6d68986dd3525fb867`  
		Last Modified: Tue, 29 Oct 2024 22:58:51 GMT  
		Size: 12.4 KB (12375 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.6-bookworm`

```console
$ docker pull julia@sha256:beacce74c44411e9ff7d3a2d9c47df8da93effa5608db5513e4b80cf8f24690a
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

### `julia:1.10.6-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:066fe3c12ab811346b53168d4e6b894296b9c05c661f1160aaab7de42ba8db48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.5 MB (211469990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:650577d6aea7bd1e50734262e6250954dd8de23f0810f8e473d5b0b46ede003d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 17 Oct 2024 00:20:30 GMT
CMD ["bash"]
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.6-linux-x86_64.tar.gz'; 			sha256='8b53429e17585c66476b39f2b2279da207ea0f310c55db38f3410bdd4f6a3d49'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.6-linux-aarch64.tar.gz'; 			sha256='5530359839544ba1ee8f6f66728fd4f9b591822c1633f93cf9672c7f9528fc3a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.6-linux-i686.tar.gz'; 			sha256='52771086511905c22669bc8667a98a97ad26e82747a429165fde2641672e962b'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.6-linux-ppc64le.tar.gz'; 			sha256='bbfd63ba2bf497f82101ef8ca3e681adca4ab95f9d5e12abfb2cf3a3c72d6126'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24730e632d102308412e50d47afc4963ab80945853c21921db804fee91f70c4`  
		Last Modified: Tue, 29 Oct 2024 22:59:04 GMT  
		Size: 5.7 MB (5712693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54df6a7b1c987a3a57cf6c3a830c3d7ded854573b58fcbbc7c8ab5d975d3241b`  
		Last Modified: Tue, 29 Oct 2024 22:59:07 GMT  
		Size: 176.6 MB (176630637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f180184aba9526edbb4fa7be6a302a437d43b29f442ab8cd3062874fa38d52a1`  
		Last Modified: Tue, 29 Oct 2024 22:59:04 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.6-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:9cd8b3fc2a11d08112901e265156ad92fec39c16bd245987c402f1ecad86f33b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11687b4578ab84520d40c7e0c43a470aed5f538a5ca0b2db7132407d16805b63`

```dockerfile
```

-	Layers:
	-	`sha256:355f0872750dee81ec05047b47e309ca3afb653edcd42237934de5be5ecc1d73`  
		Last Modified: Tue, 29 Oct 2024 22:59:04 GMT  
		Size: 2.4 MB (2449212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18cccb85b4623e7a71d4bc6d3c361bc4642429b260ba99828e8b6398a6ace30e`  
		Last Modified: Tue, 29 Oct 2024 22:59:04 GMT  
		Size: 17.0 KB (17018 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.6-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:fe90cd54fa02a1a87cd43900e84872dac0e2eb6acb158a7df97cadf542412053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.0 MB (212041217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a349d4bb79aaa181d575d5c590ea369d89d19495483c28c89cc30ed9f22f9baa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.6-linux-x86_64.tar.gz'; 			sha256='8b53429e17585c66476b39f2b2279da207ea0f310c55db38f3410bdd4f6a3d49'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.6-linux-aarch64.tar.gz'; 			sha256='5530359839544ba1ee8f6f66728fd4f9b591822c1633f93cf9672c7f9528fc3a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.6-linux-i686.tar.gz'; 			sha256='52771086511905c22669bc8667a98a97ad26e82747a429165fde2641672e962b'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.6-linux-ppc64le.tar.gz'; 			sha256='bbfd63ba2bf497f82101ef8ca3e681adca4ab95f9d5e12abfb2cf3a3c72d6126'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9f7aa12a882cbec1989b7eb39edf886c46b6ec43a0dbdaa46322fb5ea3fd09`  
		Last Modified: Wed, 30 Oct 2024 00:03:43 GMT  
		Size: 5.5 MB (5537174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba2ee9345c139face9d10e01386b6012aa72822b7e356753ae9c5a875667fad`  
		Last Modified: Wed, 30 Oct 2024 00:03:47 GMT  
		Size: 177.3 MB (177347335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1623697d698db51239d0786367179ae5b9fdda3d9646d150726d51f4d05911`  
		Last Modified: Wed, 30 Oct 2024 00:03:42 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.6-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:0713eadec1bcf05f96c35d1be3349adfdba8398cd7e7141c0c397678f7199e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ef0d98ccdd9762f43506d01f867a1a6b49cbf1c69f3de0971422f25f8d61d5`

```dockerfile
```

-	Layers:
	-	`sha256:301ab6e57c61cb7bbd0857cd1cdc41631539edf83c6f8ed5e2116b5121b95800`  
		Last Modified: Wed, 30 Oct 2024 00:03:43 GMT  
		Size: 2.4 MB (2448264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:263e7cad0f4326e8b1f9b2a1bf2ad5ca2de932f3be76f4fcc153bbfeb6859c5b`  
		Last Modified: Wed, 30 Oct 2024 00:03:42 GMT  
		Size: 17.2 KB (17155 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.6-bookworm` - linux; 386

```console
$ docker pull julia@sha256:c718d318da6995a7c5ed037813139bc5475763c90c69462b23a9c13f264071f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193827906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:142e4513d0ab21eb84ec458e70e790a6739e3398c6b63e4d2f7cf015259c8c9e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 17 Oct 2024 00:38:56 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Thu, 17 Oct 2024 00:38:56 GMT
CMD ["bash"]
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.6-linux-x86_64.tar.gz'; 			sha256='8b53429e17585c66476b39f2b2279da207ea0f310c55db38f3410bdd4f6a3d49'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.6-linux-aarch64.tar.gz'; 			sha256='5530359839544ba1ee8f6f66728fd4f9b591822c1633f93cf9672c7f9528fc3a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.6-linux-i686.tar.gz'; 			sha256='52771086511905c22669bc8667a98a97ad26e82747a429165fde2641672e962b'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.6-linux-ppc64le.tar.gz'; 			sha256='bbfd63ba2bf497f82101ef8ca3e681adca4ab95f9d5e12abfb2cf3a3c72d6126'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c544b64767c8ee9ec5202884260726a080b68fa738ff648f1936b53eb005db63`  
		Last Modified: Tue, 29 Oct 2024 22:59:02 GMT  
		Size: 5.9 MB (5870458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714cab6622ab2b57035ee3dbf90756fcc815ac79da12048a7416501899f30f15`  
		Last Modified: Tue, 29 Oct 2024 22:59:06 GMT  
		Size: 157.8 MB (157812811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135081bef526546ebd94b2b8c30a901dba8d23fb0d246f7784beecc4bcb2bf10`  
		Last Modified: Tue, 29 Oct 2024 22:59:02 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.6-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:bf6a8c8863c5670bf815c39bba3a0187df9dd2d04b885d1763f55fd9a169b1c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e27864b80a3b3c70874b2e512ecb8d105dc0ee3197d0e994acc19c4a3fbdc6e`

```dockerfile
```

-	Layers:
	-	`sha256:ec727e80c071bab5a789d0f27b0127857ca592daba008e3c2624602ffa12a9ed`  
		Last Modified: Tue, 29 Oct 2024 22:59:02 GMT  
		Size: 2.4 MB (2446304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8b8b1cbd3886057906d657ef37a305a39bc310e1a3cc8a9087fe2df9138a512`  
		Last Modified: Tue, 29 Oct 2024 22:59:02 GMT  
		Size: 17.0 KB (17011 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.6-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:c4c48e226ac08b9e19836392b0979936d62b3d7a36e84c5360d1d1b2b2d81547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.7 MB (194677985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17067b8f17bce468e0c9eeb8dc4f3ec6582dc539140ec4f27e41d606949f8b0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 17 Oct 2024 01:18:54 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Thu, 17 Oct 2024 01:18:56 GMT
CMD ["bash"]
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.6-linux-x86_64.tar.gz'; 			sha256='8b53429e17585c66476b39f2b2279da207ea0f310c55db38f3410bdd4f6a3d49'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.6-linux-aarch64.tar.gz'; 			sha256='5530359839544ba1ee8f6f66728fd4f9b591822c1633f93cf9672c7f9528fc3a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.6-linux-i686.tar.gz'; 			sha256='52771086511905c22669bc8667a98a97ad26e82747a429165fde2641672e962b'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.6-linux-ppc64le.tar.gz'; 			sha256='bbfd63ba2bf497f82101ef8ca3e681adca4ab95f9d5e12abfb2cf3a3c72d6126'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872ce7d06e1f062f97505b0e301bbfdbf0eb9be16d7514467915e735ab53c113`  
		Last Modified: Tue, 29 Oct 2024 23:01:05 GMT  
		Size: 6.2 MB (6247957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170dcc05149f98f3db1198fddc1be23f82b6ae0fcf50dd96e047466a8af395ac`  
		Last Modified: Tue, 29 Oct 2024 23:01:09 GMT  
		Size: 155.3 MB (155307456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbf0fac49cd21372305ab812b69a2b403d1f62371f492ce96e9f307669893dc`  
		Last Modified: Tue, 29 Oct 2024 23:01:04 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.6-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:605795e6f38be17a1fcaa2cfe024c183d09af212ccb061fa4ad2cf2d6b71b471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2469479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c724732b12d6ed77c9b813e7f50d05a34b89ea234bc8ceefbf789e5cf2ebcef0`

```dockerfile
```

-	Layers:
	-	`sha256:6f53f1adeb9f8fbab7623a47e3466557398985eb384c51887fbdfa6f9c1ca791`  
		Last Modified: Tue, 29 Oct 2024 23:01:05 GMT  
		Size: 2.5 MB (2452397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb684095369776335de241209d640d5a1f006b954d8abead862abffbbe157cf2`  
		Last Modified: Tue, 29 Oct 2024 23:01:04 GMT  
		Size: 17.1 KB (17082 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.6-bullseye`

```console
$ docker pull julia@sha256:d9ed59097266c0abd5e00d57846e361d1854cf794738e53579e5cb4bf23507a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.10.6-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:602199cc58de0e1f59848914cf84dee71a95eb212f6bad22fb75f5bc7ff1209a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.5 MB (210486630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6d163780e512dddadcb37f8647b74edd2f24e40c9c954067c0dacd97cda6de0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:51 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
# Thu, 17 Oct 2024 00:20:52 GMT
CMD ["bash"]
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.6-linux-x86_64.tar.gz'; 			sha256='8b53429e17585c66476b39f2b2279da207ea0f310c55db38f3410bdd4f6a3d49'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.6-linux-aarch64.tar.gz'; 			sha256='5530359839544ba1ee8f6f66728fd4f9b591822c1633f93cf9672c7f9528fc3a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.6-linux-i686.tar.gz'; 			sha256='52771086511905c22669bc8667a98a97ad26e82747a429165fde2641672e962b'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.6-linux-ppc64le.tar.gz'; 			sha256='bbfd63ba2bf497f82101ef8ca3e681adca4ab95f9d5e12abfb2cf3a3c72d6126'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24b711ff7d16b77620f37463d5955fdffc6028b0c517834f3e2b44c13f1acde`  
		Last Modified: Tue, 29 Oct 2024 22:59:07 GMT  
		Size: 2.4 MB (2426561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca054cf855c07696a5cbceb538284ec5b871d967630cba2def7b697f0b8bb0fc`  
		Last Modified: Tue, 29 Oct 2024 22:59:10 GMT  
		Size: 176.6 MB (176630899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc80302bd481b1a67cec4e3009fa2d64c00c75313b48ba2d4536cdc3b9d396e`  
		Last Modified: Tue, 29 Oct 2024 22:59:07 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.6-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:298558b1d8b65dda22bf1e4f926ca59476fe21167dfd3fc1c5ba4b0484e11135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2734071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef18ec26fa0f2ed57e23dde9b6b0b86dda90853dff90b16c917c2061f98b3ba4`

```dockerfile
```

-	Layers:
	-	`sha256:49e39ae4e4090a91039a769e05f8b2d38bb8cb63c7b0a21573d3250d35641360`  
		Last Modified: Tue, 29 Oct 2024 22:59:07 GMT  
		Size: 2.7 MB (2717617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bd8319123f41f50b738b9bea9adfe950ac5c7911904ab6619c6da965daaa5bf`  
		Last Modified: Tue, 29 Oct 2024 22:59:07 GMT  
		Size: 16.5 KB (16454 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.6-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:5a0ed26284ea162ba042b10cd0657cef6ed1ee8e33543f3b6eba58afa119ad1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.8 MB (209838984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:582f2f475e880b9f25ddc1ca8170a2947fb5ba3978b3446fb800fc65bb632c86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:13 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Thu, 17 Oct 2024 01:12:14 GMT
CMD ["bash"]
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.6-linux-x86_64.tar.gz'; 			sha256='8b53429e17585c66476b39f2b2279da207ea0f310c55db38f3410bdd4f6a3d49'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.6-linux-aarch64.tar.gz'; 			sha256='5530359839544ba1ee8f6f66728fd4f9b591822c1633f93cf9672c7f9528fc3a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.6-linux-i686.tar.gz'; 			sha256='52771086511905c22669bc8667a98a97ad26e82747a429165fde2641672e962b'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.6-linux-ppc64le.tar.gz'; 			sha256='bbfd63ba2bf497f82101ef8ca3e681adca4ab95f9d5e12abfb2cf3a3c72d6126'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8def44bdef5469eb29a86fa0a8c5904a811f78e825d26e28e2867f1953b48b20`  
		Last Modified: Wed, 30 Oct 2024 00:04:57 GMT  
		Size: 2.4 MB (2415135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce676b526ca999e66c3b1e1fc051b7f8626b6f595834e4ea894e43f4fd7d77cf`  
		Last Modified: Wed, 30 Oct 2024 00:05:01 GMT  
		Size: 177.3 MB (177347721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab419172de04012ccd11c2b4cd457b75f9ae0833fb6052fd9b05e054238f8be`  
		Last Modified: Wed, 30 Oct 2024 00:04:56 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.6-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:2b3acb7550a4e64071aad1e929ce4b0c9d2dc4401f51d20159eba52ed5053dc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2733175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e838849e3ac3a25a3ad3af62b27bb199edcd0960452ce74e1eaeaa99fc0789`

```dockerfile
```

-	Layers:
	-	`sha256:a390bb685be997573cafbe327619e268421efe9068c6882c47203144cf781b6e`  
		Last Modified: Wed, 30 Oct 2024 00:04:57 GMT  
		Size: 2.7 MB (2716633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a20066a10e7d7f68f92879db8ef288b03041321c70d57e582d7f9335987d68c`  
		Last Modified: Wed, 30 Oct 2024 00:04:56 GMT  
		Size: 16.5 KB (16542 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.6-bullseye` - linux; 386

```console
$ docker pull julia@sha256:075542375efbdea852b4788a73ace5bbc6f46ce67bb4533671810239458265c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192760616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96da4367a97ec41859b8598c03f0d979467b238c6d1d2b49f6a548b4c0f465bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 17 Oct 2024 00:39:19 GMT
ADD file:05098c6b0b4cfde8b4ffadc861fc7668bbf1779983d50b6be61989e6378fc17b in / 
# Thu, 17 Oct 2024 00:39:20 GMT
CMD ["bash"]
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.6-linux-x86_64.tar.gz'; 			sha256='8b53429e17585c66476b39f2b2279da207ea0f310c55db38f3410bdd4f6a3d49'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.6-linux-aarch64.tar.gz'; 			sha256='5530359839544ba1ee8f6f66728fd4f9b591822c1633f93cf9672c7f9528fc3a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.6-linux-i686.tar.gz'; 			sha256='52771086511905c22669bc8667a98a97ad26e82747a429165fde2641672e962b'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.6-linux-ppc64le.tar.gz'; 			sha256='bbfd63ba2bf497f82101ef8ca3e681adca4ab95f9d5e12abfb2cf3a3c72d6126'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0aff79075c186716daeb376e46e89131aa14f0dc2bd8f794bd04d72494cb4693`  
		Last Modified: Thu, 17 Oct 2024 00:43:15 GMT  
		Size: 32.4 MB (32413830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf8ae6599e3b396cdad1e37cf3e67a4baf9ec59452708eb157c5da6df26ddec`  
		Last Modified: Tue, 29 Oct 2024 22:59:08 GMT  
		Size: 2.5 MB (2532988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6781032aff8d458d7f5fd30b797d1936118b305311e91866d98bf9fc04f80150`  
		Last Modified: Tue, 29 Oct 2024 22:59:12 GMT  
		Size: 157.8 MB (157813426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55877412772a1d62133cc585994847d91e3d4d4de2dec59b22698fcf197604c6`  
		Last Modified: Tue, 29 Oct 2024 22:59:08 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.6-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:2ab9c04ae6075411f3f8d0a1cf4ef4b5329b3c26138be2bd3150ab271abaaacb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2731158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5eafa68ad6a8e6437cc4fd6d7d3f28709342c2c4f8b91676592155ceda6da40`

```dockerfile
```

-	Layers:
	-	`sha256:be884603289a6063f8bbf2088dc94bb247d9563e716c8dcb2daeb1c18f2ead3e`  
		Last Modified: Tue, 29 Oct 2024 22:59:08 GMT  
		Size: 2.7 MB (2714725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80537ad0f08f28d9da4c02ce1cdd8d65a25e1be1ecf1972c314b506724b3a7b5`  
		Last Modified: Tue, 29 Oct 2024 22:59:08 GMT  
		Size: 16.4 KB (16433 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.6-windowsservercore`

```console
$ docker pull julia@sha256:bad5fd470043108972fab03ab7fba19dd1a37e13481871a96cfaccc0c9a78304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `julia:1.10.6-windowsservercore` - windows version 10.0.20348.2762; amd64

```console
$ docker pull julia@sha256:0e742f15776e4f7e2466446691d4e7d0ae81576fea07e6ac69eea39d103d0173
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1988310186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3085046212c05c9e4b0a731e38e30128a7ac793956c2995e4417d66e1888e4b8`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Tue, 29 Oct 2024 23:56:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 29 Oct 2024 23:56:59 GMT
ENV JULIA_VERSION=1.10.6
# Tue, 29 Oct 2024 23:57:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.6-win64.exe
# Tue, 29 Oct 2024 23:57:02 GMT
ENV JULIA_SHA256=f29e62ea3edede6b9a245ca1117d5f5232a78f324902a69368e3ed5836f96d59
# Tue, 29 Oct 2024 23:59:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 29 Oct 2024 23:59:25 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a703ec8db6afe2491ab0518ad479df3ea9eb52d5967771bcebf035a59b29d6`  
		Last Modified: Tue, 29 Oct 2024 23:59:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8738f7e52db049fd38af00a87bd6e9119f5abbd70ab1bd552a1f01f9785c6b5d`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0083b70e021328f6ae7e9d213e77735279f1cf457c243584e8cea8bad89d18`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220778260973a205a267336a441e793360c94d727e8fce10de071e7edb0fa48b`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc4ea8989979e5b3bdf5bafb635c0dd5f91c792a52a23c77f353466f2dbeea3`  
		Last Modified: Tue, 29 Oct 2024 23:59:50 GMT  
		Size: 189.0 MB (188962205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ae0a51fc94fd2d69da5be3323e71e7737e28dd291e65c140e1836658098af0`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10.6-windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull julia@sha256:6ca14732d9b63fca4b7397eadd040a3c87ccd84e1ba749fb7e1ee9bc42244913
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2090791615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d349843745bd27b77509eb661965f36217fa3b818dd96f5ef8ad5d5c868c8d93`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 29 Oct 2024 22:58:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 29 Oct 2024 22:58:31 GMT
ENV JULIA_VERSION=1.10.6
# Tue, 29 Oct 2024 22:58:32 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.6-win64.exe
# Tue, 29 Oct 2024 22:58:33 GMT
ENV JULIA_SHA256=f29e62ea3edede6b9a245ca1117d5f5232a78f324902a69368e3ed5836f96d59
# Tue, 29 Oct 2024 23:00:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 29 Oct 2024 23:00:38 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187f98b1f55258e314fedb9c2f6226e1c2a11740febbd0ce89d238e43c0bed2`  
		Last Modified: Tue, 29 Oct 2024 23:00:43 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba0606836b66ce8f497eac48f690ee807b532d6777b4e56ce704dd15e77e678a`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9b820753126ccfc32f3fba865e5d5b4824aedcdaf3831831d2844d43d919f6`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0726905f5fbf316e8c8c6741bc1793dde3958dca4f53a28ff39972d4253b31`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88eff14262dc220189629e33a16987149944ad23b1b5f939113fa634c51f7f4b`  
		Last Modified: Tue, 29 Oct 2024 23:01:04 GMT  
		Size: 189.0 MB (188959879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a37e9e4b5cd836f0416d006af1817bf06ea1be011782932bf2b3785e6a08c44`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.6-windowsservercore-1809`

```console
$ docker pull julia@sha256:58087ae2d9648fa6b36d657e915e543117eeae1bb7dd7ecd19ab015510e67d32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `julia:1.10.6-windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull julia@sha256:6ca14732d9b63fca4b7397eadd040a3c87ccd84e1ba749fb7e1ee9bc42244913
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2090791615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d349843745bd27b77509eb661965f36217fa3b818dd96f5ef8ad5d5c868c8d93`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 29 Oct 2024 22:58:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 29 Oct 2024 22:58:31 GMT
ENV JULIA_VERSION=1.10.6
# Tue, 29 Oct 2024 22:58:32 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.6-win64.exe
# Tue, 29 Oct 2024 22:58:33 GMT
ENV JULIA_SHA256=f29e62ea3edede6b9a245ca1117d5f5232a78f324902a69368e3ed5836f96d59
# Tue, 29 Oct 2024 23:00:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 29 Oct 2024 23:00:38 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187f98b1f55258e314fedb9c2f6226e1c2a11740febbd0ce89d238e43c0bed2`  
		Last Modified: Tue, 29 Oct 2024 23:00:43 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba0606836b66ce8f497eac48f690ee807b532d6777b4e56ce704dd15e77e678a`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9b820753126ccfc32f3fba865e5d5b4824aedcdaf3831831d2844d43d919f6`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0726905f5fbf316e8c8c6741bc1793dde3958dca4f53a28ff39972d4253b31`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88eff14262dc220189629e33a16987149944ad23b1b5f939113fa634c51f7f4b`  
		Last Modified: Tue, 29 Oct 2024 23:01:04 GMT  
		Size: 189.0 MB (188959879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a37e9e4b5cd836f0416d006af1817bf06ea1be011782932bf2b3785e6a08c44`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.6-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:0e65c00e6c1db3fd045c6a7adc21172ef95b4163656cc090fe6155b59939459c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `julia:1.10.6-windowsservercore-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull julia@sha256:0e742f15776e4f7e2466446691d4e7d0ae81576fea07e6ac69eea39d103d0173
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1988310186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3085046212c05c9e4b0a731e38e30128a7ac793956c2995e4417d66e1888e4b8`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Tue, 29 Oct 2024 23:56:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 29 Oct 2024 23:56:59 GMT
ENV JULIA_VERSION=1.10.6
# Tue, 29 Oct 2024 23:57:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.6-win64.exe
# Tue, 29 Oct 2024 23:57:02 GMT
ENV JULIA_SHA256=f29e62ea3edede6b9a245ca1117d5f5232a78f324902a69368e3ed5836f96d59
# Tue, 29 Oct 2024 23:59:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 29 Oct 2024 23:59:25 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a703ec8db6afe2491ab0518ad479df3ea9eb52d5967771bcebf035a59b29d6`  
		Last Modified: Tue, 29 Oct 2024 23:59:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8738f7e52db049fd38af00a87bd6e9119f5abbd70ab1bd552a1f01f9785c6b5d`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0083b70e021328f6ae7e9d213e77735279f1cf457c243584e8cea8bad89d18`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220778260973a205a267336a441e793360c94d727e8fce10de071e7edb0fa48b`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc4ea8989979e5b3bdf5bafb635c0dd5f91c792a52a23c77f353466f2dbeea3`  
		Last Modified: Tue, 29 Oct 2024 23:59:50 GMT  
		Size: 189.0 MB (188962205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ae0a51fc94fd2d69da5be3323e71e7737e28dd291e65c140e1836658098af0`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11`

```console
$ docker pull julia@sha256:59ccf7b59abf7f7d78813b5fb0e244b0c7830c5656b956f9fde7bd27626476c0
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
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `julia:1.11` - linux; amd64

```console
$ docker pull julia@sha256:fd3a4e95d341cae23b3aef5fcf9fec1d2ee96fd1f1e3bcd6aa64643563ae314f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291937349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ea47312db572c60c8c9351c6b9a422aea6833da9717e5db4e3ea5f32f51b2dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
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
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bb87bd1b2a94a1a42597777f17fe57ac41a63e9ac4631763f29cc1c4eb7971`  
		Last Modified: Thu, 17 Oct 2024 01:21:28 GMT  
		Size: 5.7 MB (5712680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4115daba408d4d475ca265cb576361ce9cf9b002176e4268ae5a0b3eb9853f`  
		Last Modified: Thu, 17 Oct 2024 01:21:36 GMT  
		Size: 257.1 MB (257098011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dff1f91cca18ab23d091ade6d0b0385a0c6050a8fc43fb5a8159e253ae8121b`  
		Last Modified: Thu, 17 Oct 2024 01:21:28 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:57ae5db18ee250b23a45ccc6fdfd5ccfee4d8c87efaf4d1abd057f2769a0329c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2453853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4337eaa6caa92128ea6fc9c7c22d4a311aa67f379c859d92b14a3d50d64a8df7`

```dockerfile
```

-	Layers:
	-	`sha256:63f5d166f6304023b2c389e225252262af1d10b62688335ff269f55508f042ec`  
		Last Modified: Thu, 17 Oct 2024 01:21:28 GMT  
		Size: 2.4 MB (2435621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:065c1f726a44cdf9df5e738e56cd81c29b434fbd47bd7d3361c1137f08dd4cfd`  
		Last Modified: Thu, 17 Oct 2024 01:21:28 GMT  
		Size: 18.2 KB (18232 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:a2491aa90ba329dafe060d6adb24cb3fb83e36f4c4286633692e583097db3c36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.7 MB (288700700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4129f7f55b30d16e8139c69a813236f23e65139288d9ee0075399d5f6b89e8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
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
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f005b595846e0cdd9b8d61bffb35f19c8e42003b09c6fa5d02f40d76d40d3142`  
		Last Modified: Thu, 17 Oct 2024 13:15:23 GMT  
		Size: 5.5 MB (5537166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c05e13caa8823e23d317536ff1d1dd1796fe2a83847ee02d6db48a22ba0646a`  
		Last Modified: Thu, 17 Oct 2024 13:15:28 GMT  
		Size: 254.0 MB (254006821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a62b6e4f6fa18765799cd22bcbae3f15f20072e9ae053bbdf98a3efe82f52df`  
		Last Modified: Thu, 17 Oct 2024 13:15:23 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:e36e79625d4b2f06ab1b7414a9487e294e789f55949c056a20ab07b607eebe13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2454336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8494e45d3412b161773bf9c522b57e83aa21c819be146fb56574805aae74dfcf`

```dockerfile
```

-	Layers:
	-	`sha256:e348b3b6b5b4e6f22acb995010c94ad138b49e91b49459d7330ea9c665239067`  
		Last Modified: Thu, 17 Oct 2024 13:15:23 GMT  
		Size: 2.4 MB (2435943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f241bd181640f964b873b1a39186238e3c1e3853e6238c3a768fc63f04bd97fc`  
		Last Modified: Thu, 17 Oct 2024 13:15:23 GMT  
		Size: 18.4 KB (18393 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - linux; 386

```console
$ docker pull julia@sha256:9664f1d3532459c67196e66b0da1c613348bb1cf1a7dc1c9db5e84315309012c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270672761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e604fb4f328efb8dfd2637df284176512ed1ed6b6c31def9ebcf21aec0c2b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
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
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef46da67fc6417b2c8511177a2f904986a28c82f5f3980c4a3bdda412a0cb96`  
		Last Modified: Thu, 17 Oct 2024 01:21:34 GMT  
		Size: 5.9 MB (5870476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8aa1a2f42b1e06e545c1b61c842a6ba6a571d450dcdddb64e06db764fe22c5c`  
		Last Modified: Thu, 17 Oct 2024 01:21:41 GMT  
		Size: 234.7 MB (234657651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5922d12011579acdb276facae35eb217cd417b8ec2ca21c0b5425fbce9957824`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:5eb0819bd9c824da83af57c0bc587134d66e1189b39e553b460a89a42bdffc69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2450874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4631426bd2f8080a85a75feec2e4cf79652d64624da9905f16d08a1587d6ad79`

```dockerfile
```

-	Layers:
	-	`sha256:fafe3fc46d504391631a308525c4ffbde1b21fc417b2faec508a98df7b15e1ee`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 2.4 MB (2432693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8863f51017c0640fb041800f19fb46fdfab92ec6c3729f6040e84fe38b66c4ed`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 18.2 KB (18181 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - linux; ppc64le

```console
$ docker pull julia@sha256:f1ffa4874e6d100fc1fdce7ae8cff75b4e3cddc3a7063b68467942ab0e7b2d8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.8 MB (283845662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad3f11c30a7d695a2d9d6b9c71b233a341fa06c2f6602447727e3a85aedab3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
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
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ce3688624a92ce5984769ec19a8b421d5cbfdd057e1e30bf5e57cada049215`  
		Last Modified: Thu, 17 Oct 2024 08:42:06 GMT  
		Size: 6.2 MB (6247943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a24702a300837b63b3c298602a67686d45b25deb56363aa065d299c9bdd29b1`  
		Last Modified: Thu, 17 Oct 2024 08:42:14 GMT  
		Size: 244.5 MB (244475147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a582dd71509d2a88c872a94ed8a67e73c053144e9c5664720588c7684748c068`  
		Last Modified: Thu, 17 Oct 2024 08:42:05 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:d6cbf0fa8a4870af9ee3181a941d82be8d58199b70f220a63dd91c918affbbde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2458348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa065e6917f5d7c47bd2416298a0c99812e31e2ddaa68483848ff93690e8f736`

```dockerfile
```

-	Layers:
	-	`sha256:3abe2457e038cfc98e2170b01d92cd1b40f47bfa8cf991cc1220a0da68f000d7`  
		Last Modified: Thu, 17 Oct 2024 08:42:06 GMT  
		Size: 2.4 MB (2440052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4312eae9f6f8c06593b79106a3f06b6ce65b15ecf3c05fce5aba31afba073be7`  
		Last Modified: Thu, 17 Oct 2024 08:42:05 GMT  
		Size: 18.3 KB (18296 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - windows version 10.0.20348.2762; amd64

```console
$ docker pull julia@sha256:1aadbfaaaab1ead9b289075e1c50a66c24e73f0abb54ff58987658fb3d721339
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2052417149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73d77c77c9074ad1a6ef6af5f3c75625db9c5be5d552e03bdfb712643fa3262`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Thu, 17 Oct 2024 00:07:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:07:44 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:07:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:07:46 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:09:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:09:05 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7310b1b784f497ecef75a191c3fdf858c6c5e7102326517af7e9c8f4a9ba2ab`  
		Last Modified: Thu, 17 Oct 2024 00:09:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8f60354745986b41d1c97227046f1bf77a40a1b841e2b733d28d9f336d0517a`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81f4ad3b9ee5bb6c5bcf302663adf9404aed5f2a775c97739ddeaf04c390105`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e95309645bd9402810abb1f62e8d28e2eb50ad30d923ac5635718caafc953f3`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1f65e1c7b97054a3ff76d9eb10192f3ffb9f984e554d5dad56b1deffa4a26e`  
		Last Modified: Thu, 17 Oct 2024 00:09:40 GMT  
		Size: 253.1 MB (253069135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3efcc69a49a46842179fb8d2b256e3aca046c05572afb9537e9e68808da649`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11` - windows version 10.0.17763.6414; amd64

```console
$ docker pull julia@sha256:5f7b3fa057a3f34c286a0c29544e30b8e25de7d389fcb9a7c39e5dbc2ac59431
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2154909599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73428e1a2c97df8e870d60c63531878514df329661819a1917855fe9c852deb3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Thu, 17 Oct 2024 00:04:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:04:47 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:06:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:06:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4316cb4a890d1430c8dbb6f02f1ed4b07cc1f84668ddfe58d132e70173591231`  
		Last Modified: Thu, 17 Oct 2024 00:06:49 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed07735f2e4d115dbc648a3fbf628ee5e173125dcd63d695a85f30c2d701668d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02cf70042980e2e6296807674462b486e411ba5e80ecf7c6ec3bdd5e0e7a5085`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1c8839b71fde8692b035b2f54ea4a7c21650e10ae20680a0ba68b723b9e57d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4afde2ddc271e774c969b81b72e4ec22aa664487988ca09a851e16930efb47`  
		Last Modified: Thu, 17 Oct 2024 00:07:18 GMT  
		Size: 253.1 MB (253077851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f694e951fd639e6dc35a1e43dce74e5247712830c183397156d8b0ff48747470`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-bookworm`

```console
$ docker pull julia@sha256:33cde3f7aaea90daa3bbb93d1a002daf679b68380a9cc24420b90e2c88382d36
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

### `julia:1.11-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:fd3a4e95d341cae23b3aef5fcf9fec1d2ee96fd1f1e3bcd6aa64643563ae314f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291937349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ea47312db572c60c8c9351c6b9a422aea6833da9717e5db4e3ea5f32f51b2dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
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
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bb87bd1b2a94a1a42597777f17fe57ac41a63e9ac4631763f29cc1c4eb7971`  
		Last Modified: Thu, 17 Oct 2024 01:21:28 GMT  
		Size: 5.7 MB (5712680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4115daba408d4d475ca265cb576361ce9cf9b002176e4268ae5a0b3eb9853f`  
		Last Modified: Thu, 17 Oct 2024 01:21:36 GMT  
		Size: 257.1 MB (257098011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dff1f91cca18ab23d091ade6d0b0385a0c6050a8fc43fb5a8159e253ae8121b`  
		Last Modified: Thu, 17 Oct 2024 01:21:28 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:57ae5db18ee250b23a45ccc6fdfd5ccfee4d8c87efaf4d1abd057f2769a0329c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2453853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4337eaa6caa92128ea6fc9c7c22d4a311aa67f379c859d92b14a3d50d64a8df7`

```dockerfile
```

-	Layers:
	-	`sha256:63f5d166f6304023b2c389e225252262af1d10b62688335ff269f55508f042ec`  
		Last Modified: Thu, 17 Oct 2024 01:21:28 GMT  
		Size: 2.4 MB (2435621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:065c1f726a44cdf9df5e738e56cd81c29b434fbd47bd7d3361c1137f08dd4cfd`  
		Last Modified: Thu, 17 Oct 2024 01:21:28 GMT  
		Size: 18.2 KB (18232 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:a2491aa90ba329dafe060d6adb24cb3fb83e36f4c4286633692e583097db3c36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.7 MB (288700700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4129f7f55b30d16e8139c69a813236f23e65139288d9ee0075399d5f6b89e8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
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
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f005b595846e0cdd9b8d61bffb35f19c8e42003b09c6fa5d02f40d76d40d3142`  
		Last Modified: Thu, 17 Oct 2024 13:15:23 GMT  
		Size: 5.5 MB (5537166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c05e13caa8823e23d317536ff1d1dd1796fe2a83847ee02d6db48a22ba0646a`  
		Last Modified: Thu, 17 Oct 2024 13:15:28 GMT  
		Size: 254.0 MB (254006821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a62b6e4f6fa18765799cd22bcbae3f15f20072e9ae053bbdf98a3efe82f52df`  
		Last Modified: Thu, 17 Oct 2024 13:15:23 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:e36e79625d4b2f06ab1b7414a9487e294e789f55949c056a20ab07b607eebe13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2454336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8494e45d3412b161773bf9c522b57e83aa21c819be146fb56574805aae74dfcf`

```dockerfile
```

-	Layers:
	-	`sha256:e348b3b6b5b4e6f22acb995010c94ad138b49e91b49459d7330ea9c665239067`  
		Last Modified: Thu, 17 Oct 2024 13:15:23 GMT  
		Size: 2.4 MB (2435943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f241bd181640f964b873b1a39186238e3c1e3853e6238c3a768fc63f04bd97fc`  
		Last Modified: Thu, 17 Oct 2024 13:15:23 GMT  
		Size: 18.4 KB (18393 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bookworm` - linux; 386

```console
$ docker pull julia@sha256:9664f1d3532459c67196e66b0da1c613348bb1cf1a7dc1c9db5e84315309012c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270672761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e604fb4f328efb8dfd2637df284176512ed1ed6b6c31def9ebcf21aec0c2b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
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
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef46da67fc6417b2c8511177a2f904986a28c82f5f3980c4a3bdda412a0cb96`  
		Last Modified: Thu, 17 Oct 2024 01:21:34 GMT  
		Size: 5.9 MB (5870476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8aa1a2f42b1e06e545c1b61c842a6ba6a571d450dcdddb64e06db764fe22c5c`  
		Last Modified: Thu, 17 Oct 2024 01:21:41 GMT  
		Size: 234.7 MB (234657651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5922d12011579acdb276facae35eb217cd417b8ec2ca21c0b5425fbce9957824`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:5eb0819bd9c824da83af57c0bc587134d66e1189b39e553b460a89a42bdffc69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2450874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4631426bd2f8080a85a75feec2e4cf79652d64624da9905f16d08a1587d6ad79`

```dockerfile
```

-	Layers:
	-	`sha256:fafe3fc46d504391631a308525c4ffbde1b21fc417b2faec508a98df7b15e1ee`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 2.4 MB (2432693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8863f51017c0640fb041800f19fb46fdfab92ec6c3729f6040e84fe38b66c4ed`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 18.2 KB (18181 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:f1ffa4874e6d100fc1fdce7ae8cff75b4e3cddc3a7063b68467942ab0e7b2d8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.8 MB (283845662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad3f11c30a7d695a2d9d6b9c71b233a341fa06c2f6602447727e3a85aedab3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
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
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ce3688624a92ce5984769ec19a8b421d5cbfdd057e1e30bf5e57cada049215`  
		Last Modified: Thu, 17 Oct 2024 08:42:06 GMT  
		Size: 6.2 MB (6247943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a24702a300837b63b3c298602a67686d45b25deb56363aa065d299c9bdd29b1`  
		Last Modified: Thu, 17 Oct 2024 08:42:14 GMT  
		Size: 244.5 MB (244475147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a582dd71509d2a88c872a94ed8a67e73c053144e9c5664720588c7684748c068`  
		Last Modified: Thu, 17 Oct 2024 08:42:05 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:d6cbf0fa8a4870af9ee3181a941d82be8d58199b70f220a63dd91c918affbbde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2458348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa065e6917f5d7c47bd2416298a0c99812e31e2ddaa68483848ff93690e8f736`

```dockerfile
```

-	Layers:
	-	`sha256:3abe2457e038cfc98e2170b01d92cd1b40f47bfa8cf991cc1220a0da68f000d7`  
		Last Modified: Thu, 17 Oct 2024 08:42:06 GMT  
		Size: 2.4 MB (2440052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4312eae9f6f8c06593b79106a3f06b6ce65b15ecf3c05fce5aba31afba073be7`  
		Last Modified: Thu, 17 Oct 2024 08:42:05 GMT  
		Size: 18.3 KB (18296 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11-bullseye`

```console
$ docker pull julia@sha256:d8596315fc3f33f87595593bf6d6c24e7175f1ba2247551b566d73824426057e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.11-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:89b0252e81fcee8a8295a302dfbd5333ebf5fc9b2bbcbf21dd0dd432df83bd5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (290953918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c5e3b2a9d92441caccba1899fdfadb95145c7b3454af5d79cc49eef8a2b12dd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
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
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1678fe3cd4a658f476437fee9e77b0c2086786926a90c07b083d0343a3675d34`  
		Last Modified: Thu, 17 Oct 2024 01:21:31 GMT  
		Size: 2.4 MB (2426579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13bf3dac7e14a600162ea26186e3f4f9e2eb67b797a698ca137e9bda78be3095`  
		Last Modified: Thu, 17 Oct 2024 01:21:34 GMT  
		Size: 257.1 MB (257098167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24eeabef1fc4078b2230b57296e3885ca5a8abe902842a963d54dd9229da645`  
		Last Modified: Thu, 17 Oct 2024 01:21:31 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:67cb263e6e9c5a8df2d07f56530084b32aa0fa18b9f54e1c70633d08ee81508f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e7a2b55d44957d73538f15728c85350a58a54b6670423e772b5052af5b609b`

```dockerfile
```

-	Layers:
	-	`sha256:e404b3ce366a6055b639f0e587f8f22d969c64c22ecac08b317416e03980c296`  
		Last Modified: Thu, 17 Oct 2024 01:21:31 GMT  
		Size: 2.7 MB (2703232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1cca66d1ab6aee6b83ad8e00220188da64a51b78924668d3a5d499b22c95b52`  
		Last Modified: Thu, 17 Oct 2024 01:21:31 GMT  
		Size: 17.1 KB (17061 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4f7f024b62a8f78c7294efa5ae1766b248b3bdf7b9bbb5e9c1416e4e8d1d84fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286497932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e390fcde5664778999f291f06fae01e77921743114fe33fdc45f3115c43c11dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
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
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a413099e7fe61ccf8c3081b040fa09c50cbc6a831480a5614a60a0d3c69b56b8`  
		Last Modified: Thu, 17 Oct 2024 13:16:53 GMT  
		Size: 2.4 MB (2415124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ec42daf214f0d308f8292a6037cc8f045cfdc9adfe28ff544cc0fb9a87b67a`  
		Last Modified: Thu, 17 Oct 2024 13:16:59 GMT  
		Size: 254.0 MB (254006680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a03157b90421e9af495118fb5dd03f42dc3a8de569955b88ad28a1def229884`  
		Last Modified: Thu, 17 Oct 2024 13:16:53 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:37c0ceb7fd6b428c7ce243fdeb9373c1099770d26ebc891187c07606979b3708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d376da6f82e6ccf88c0c94e1cd0081b3dd5ecd7135c4e0a073360dd2f42e4009`

```dockerfile
```

-	Layers:
	-	`sha256:379457b9725569536171521dfa577f8872f6d6231c665f670eb96bc047caa7e1`  
		Last Modified: Thu, 17 Oct 2024 13:16:53 GMT  
		Size: 2.7 MB (2703494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1b312173fb754b10124c5b9d4a848af7c804fd34ba816a297562afe8a0b0353`  
		Last Modified: Thu, 17 Oct 2024 13:16:53 GMT  
		Size: 17.2 KB (17174 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bullseye` - linux; 386

```console
$ docker pull julia@sha256:3670a732c97cffad25985d92fbb803b9b874eca1f6e26a4f56d8a77c91c1deea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.6 MB (269605951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bb8f95ee66c50d9e825aedeb3254da01eaa7c893aec91624b016ac95a35fe7c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD file:05098c6b0b4cfde8b4ffadc861fc7668bbf1779983d50b6be61989e6378fc17b in / 
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
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
	-	`sha256:0aff79075c186716daeb376e46e89131aa14f0dc2bd8f794bd04d72494cb4693`  
		Last Modified: Thu, 17 Oct 2024 00:43:15 GMT  
		Size: 32.4 MB (32413830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351b630321cf786277448e0f7aea94f99fc611feec697422839581d6ba78b0f4`  
		Last Modified: Thu, 17 Oct 2024 01:14:36 GMT  
		Size: 2.5 MB (2533097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a25ec52f239ad17072bdbca92923baca090ca0beb325e15e8b38ec0d9a07bb6`  
		Last Modified: Thu, 17 Oct 2024 01:14:41 GMT  
		Size: 234.7 MB (234658656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacaf77ce79d2cad5f10ebb5c0a2cf0132caef0f18a13b0397f5419a1b104dae`  
		Last Modified: Thu, 17 Oct 2024 01:14:36 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:801107f4fb9fa1d75ece047478ee52a0cde10e3e985cb4235e707647835d9385
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2717361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a242ec47f9cd91c5c05a334d40ffb11921f23481e6fca0e70c18cee75e1be40`

```dockerfile
```

-	Layers:
	-	`sha256:2a3f27893e3c035da08f3858e8b8d9e3d748d8c2d2a8354fba0c038570df9fc1`  
		Last Modified: Thu, 17 Oct 2024 01:14:36 GMT  
		Size: 2.7 MB (2700330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1c148b1faeb4d330bc4cb1657a099ca6c996d5624aa2a62d3c3945b9e70e713`  
		Last Modified: Thu, 17 Oct 2024 01:14:36 GMT  
		Size: 17.0 KB (17031 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11-windowsservercore`

```console
$ docker pull julia@sha256:d36dd547370e9fd68c4f5dc635f8c3ea0da809f71f508a8724c909f927574ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `julia:1.11-windowsservercore` - windows version 10.0.20348.2762; amd64

```console
$ docker pull julia@sha256:1aadbfaaaab1ead9b289075e1c50a66c24e73f0abb54ff58987658fb3d721339
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2052417149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73d77c77c9074ad1a6ef6af5f3c75625db9c5be5d552e03bdfb712643fa3262`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Thu, 17 Oct 2024 00:07:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:07:44 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:07:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:07:46 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:09:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:09:05 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7310b1b784f497ecef75a191c3fdf858c6c5e7102326517af7e9c8f4a9ba2ab`  
		Last Modified: Thu, 17 Oct 2024 00:09:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8f60354745986b41d1c97227046f1bf77a40a1b841e2b733d28d9f336d0517a`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81f4ad3b9ee5bb6c5bcf302663adf9404aed5f2a775c97739ddeaf04c390105`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e95309645bd9402810abb1f62e8d28e2eb50ad30d923ac5635718caafc953f3`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1f65e1c7b97054a3ff76d9eb10192f3ffb9f984e554d5dad56b1deffa4a26e`  
		Last Modified: Thu, 17 Oct 2024 00:09:40 GMT  
		Size: 253.1 MB (253069135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3efcc69a49a46842179fb8d2b256e3aca046c05572afb9537e9e68808da649`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11-windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull julia@sha256:5f7b3fa057a3f34c286a0c29544e30b8e25de7d389fcb9a7c39e5dbc2ac59431
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2154909599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73428e1a2c97df8e870d60c63531878514df329661819a1917855fe9c852deb3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Thu, 17 Oct 2024 00:04:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:04:47 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:06:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:06:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4316cb4a890d1430c8dbb6f02f1ed4b07cc1f84668ddfe58d132e70173591231`  
		Last Modified: Thu, 17 Oct 2024 00:06:49 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed07735f2e4d115dbc648a3fbf628ee5e173125dcd63d695a85f30c2d701668d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02cf70042980e2e6296807674462b486e411ba5e80ecf7c6ec3bdd5e0e7a5085`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1c8839b71fde8692b035b2f54ea4a7c21650e10ae20680a0ba68b723b9e57d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4afde2ddc271e774c969b81b72e4ec22aa664487988ca09a851e16930efb47`  
		Last Modified: Thu, 17 Oct 2024 00:07:18 GMT  
		Size: 253.1 MB (253077851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f694e951fd639e6dc35a1e43dce74e5247712830c183397156d8b0ff48747470`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-windowsservercore-1809`

```console
$ docker pull julia@sha256:a114dd8364b3c4135706a0b323f71e0e649bff9cf95ae8300f0378d0951c131e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `julia:1.11-windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull julia@sha256:5f7b3fa057a3f34c286a0c29544e30b8e25de7d389fcb9a7c39e5dbc2ac59431
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2154909599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73428e1a2c97df8e870d60c63531878514df329661819a1917855fe9c852deb3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Thu, 17 Oct 2024 00:04:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:04:47 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:06:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:06:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4316cb4a890d1430c8dbb6f02f1ed4b07cc1f84668ddfe58d132e70173591231`  
		Last Modified: Thu, 17 Oct 2024 00:06:49 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed07735f2e4d115dbc648a3fbf628ee5e173125dcd63d695a85f30c2d701668d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02cf70042980e2e6296807674462b486e411ba5e80ecf7c6ec3bdd5e0e7a5085`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1c8839b71fde8692b035b2f54ea4a7c21650e10ae20680a0ba68b723b9e57d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4afde2ddc271e774c969b81b72e4ec22aa664487988ca09a851e16930efb47`  
		Last Modified: Thu, 17 Oct 2024 00:07:18 GMT  
		Size: 253.1 MB (253077851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f694e951fd639e6dc35a1e43dce74e5247712830c183397156d8b0ff48747470`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:e457f763ca8c5fe3e8a20dd1a3cbf00134231b70f5070b6fa7ce67ff9536e8dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `julia:1.11-windowsservercore-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull julia@sha256:1aadbfaaaab1ead9b289075e1c50a66c24e73f0abb54ff58987658fb3d721339
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2052417149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73d77c77c9074ad1a6ef6af5f3c75625db9c5be5d552e03bdfb712643fa3262`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Thu, 17 Oct 2024 00:07:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:07:44 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:07:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:07:46 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:09:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:09:05 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7310b1b784f497ecef75a191c3fdf858c6c5e7102326517af7e9c8f4a9ba2ab`  
		Last Modified: Thu, 17 Oct 2024 00:09:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8f60354745986b41d1c97227046f1bf77a40a1b841e2b733d28d9f336d0517a`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81f4ad3b9ee5bb6c5bcf302663adf9404aed5f2a775c97739ddeaf04c390105`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e95309645bd9402810abb1f62e8d28e2eb50ad30d923ac5635718caafc953f3`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1f65e1c7b97054a3ff76d9eb10192f3ffb9f984e554d5dad56b1deffa4a26e`  
		Last Modified: Thu, 17 Oct 2024 00:09:40 GMT  
		Size: 253.1 MB (253069135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3efcc69a49a46842179fb8d2b256e3aca046c05572afb9537e9e68808da649`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.1`

```console
$ docker pull julia@sha256:59ccf7b59abf7f7d78813b5fb0e244b0c7830c5656b956f9fde7bd27626476c0
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
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `julia:1.11.1` - linux; amd64

```console
$ docker pull julia@sha256:fd3a4e95d341cae23b3aef5fcf9fec1d2ee96fd1f1e3bcd6aa64643563ae314f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291937349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ea47312db572c60c8c9351c6b9a422aea6833da9717e5db4e3ea5f32f51b2dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
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
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bb87bd1b2a94a1a42597777f17fe57ac41a63e9ac4631763f29cc1c4eb7971`  
		Last Modified: Thu, 17 Oct 2024 01:21:28 GMT  
		Size: 5.7 MB (5712680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4115daba408d4d475ca265cb576361ce9cf9b002176e4268ae5a0b3eb9853f`  
		Last Modified: Thu, 17 Oct 2024 01:21:36 GMT  
		Size: 257.1 MB (257098011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dff1f91cca18ab23d091ade6d0b0385a0c6050a8fc43fb5a8159e253ae8121b`  
		Last Modified: Thu, 17 Oct 2024 01:21:28 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.1` - unknown; unknown

```console
$ docker pull julia@sha256:57ae5db18ee250b23a45ccc6fdfd5ccfee4d8c87efaf4d1abd057f2769a0329c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2453853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4337eaa6caa92128ea6fc9c7c22d4a311aa67f379c859d92b14a3d50d64a8df7`

```dockerfile
```

-	Layers:
	-	`sha256:63f5d166f6304023b2c389e225252262af1d10b62688335ff269f55508f042ec`  
		Last Modified: Thu, 17 Oct 2024 01:21:28 GMT  
		Size: 2.4 MB (2435621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:065c1f726a44cdf9df5e738e56cd81c29b434fbd47bd7d3361c1137f08dd4cfd`  
		Last Modified: Thu, 17 Oct 2024 01:21:28 GMT  
		Size: 18.2 KB (18232 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.1` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:a2491aa90ba329dafe060d6adb24cb3fb83e36f4c4286633692e583097db3c36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.7 MB (288700700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4129f7f55b30d16e8139c69a813236f23e65139288d9ee0075399d5f6b89e8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
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
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f005b595846e0cdd9b8d61bffb35f19c8e42003b09c6fa5d02f40d76d40d3142`  
		Last Modified: Thu, 17 Oct 2024 13:15:23 GMT  
		Size: 5.5 MB (5537166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c05e13caa8823e23d317536ff1d1dd1796fe2a83847ee02d6db48a22ba0646a`  
		Last Modified: Thu, 17 Oct 2024 13:15:28 GMT  
		Size: 254.0 MB (254006821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a62b6e4f6fa18765799cd22bcbae3f15f20072e9ae053bbdf98a3efe82f52df`  
		Last Modified: Thu, 17 Oct 2024 13:15:23 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.1` - unknown; unknown

```console
$ docker pull julia@sha256:e36e79625d4b2f06ab1b7414a9487e294e789f55949c056a20ab07b607eebe13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2454336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8494e45d3412b161773bf9c522b57e83aa21c819be146fb56574805aae74dfcf`

```dockerfile
```

-	Layers:
	-	`sha256:e348b3b6b5b4e6f22acb995010c94ad138b49e91b49459d7330ea9c665239067`  
		Last Modified: Thu, 17 Oct 2024 13:15:23 GMT  
		Size: 2.4 MB (2435943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f241bd181640f964b873b1a39186238e3c1e3853e6238c3a768fc63f04bd97fc`  
		Last Modified: Thu, 17 Oct 2024 13:15:23 GMT  
		Size: 18.4 KB (18393 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.1` - linux; 386

```console
$ docker pull julia@sha256:9664f1d3532459c67196e66b0da1c613348bb1cf1a7dc1c9db5e84315309012c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270672761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e604fb4f328efb8dfd2637df284176512ed1ed6b6c31def9ebcf21aec0c2b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
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
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef46da67fc6417b2c8511177a2f904986a28c82f5f3980c4a3bdda412a0cb96`  
		Last Modified: Thu, 17 Oct 2024 01:21:34 GMT  
		Size: 5.9 MB (5870476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8aa1a2f42b1e06e545c1b61c842a6ba6a571d450dcdddb64e06db764fe22c5c`  
		Last Modified: Thu, 17 Oct 2024 01:21:41 GMT  
		Size: 234.7 MB (234657651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5922d12011579acdb276facae35eb217cd417b8ec2ca21c0b5425fbce9957824`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.1` - unknown; unknown

```console
$ docker pull julia@sha256:5eb0819bd9c824da83af57c0bc587134d66e1189b39e553b460a89a42bdffc69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2450874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4631426bd2f8080a85a75feec2e4cf79652d64624da9905f16d08a1587d6ad79`

```dockerfile
```

-	Layers:
	-	`sha256:fafe3fc46d504391631a308525c4ffbde1b21fc417b2faec508a98df7b15e1ee`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 2.4 MB (2432693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8863f51017c0640fb041800f19fb46fdfab92ec6c3729f6040e84fe38b66c4ed`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 18.2 KB (18181 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.1` - linux; ppc64le

```console
$ docker pull julia@sha256:f1ffa4874e6d100fc1fdce7ae8cff75b4e3cddc3a7063b68467942ab0e7b2d8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.8 MB (283845662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad3f11c30a7d695a2d9d6b9c71b233a341fa06c2f6602447727e3a85aedab3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
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
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ce3688624a92ce5984769ec19a8b421d5cbfdd057e1e30bf5e57cada049215`  
		Last Modified: Thu, 17 Oct 2024 08:42:06 GMT  
		Size: 6.2 MB (6247943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a24702a300837b63b3c298602a67686d45b25deb56363aa065d299c9bdd29b1`  
		Last Modified: Thu, 17 Oct 2024 08:42:14 GMT  
		Size: 244.5 MB (244475147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a582dd71509d2a88c872a94ed8a67e73c053144e9c5664720588c7684748c068`  
		Last Modified: Thu, 17 Oct 2024 08:42:05 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.1` - unknown; unknown

```console
$ docker pull julia@sha256:d6cbf0fa8a4870af9ee3181a941d82be8d58199b70f220a63dd91c918affbbde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2458348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa065e6917f5d7c47bd2416298a0c99812e31e2ddaa68483848ff93690e8f736`

```dockerfile
```

-	Layers:
	-	`sha256:3abe2457e038cfc98e2170b01d92cd1b40f47bfa8cf991cc1220a0da68f000d7`  
		Last Modified: Thu, 17 Oct 2024 08:42:06 GMT  
		Size: 2.4 MB (2440052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4312eae9f6f8c06593b79106a3f06b6ce65b15ecf3c05fce5aba31afba073be7`  
		Last Modified: Thu, 17 Oct 2024 08:42:05 GMT  
		Size: 18.3 KB (18296 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.1` - windows version 10.0.20348.2762; amd64

```console
$ docker pull julia@sha256:1aadbfaaaab1ead9b289075e1c50a66c24e73f0abb54ff58987658fb3d721339
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2052417149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73d77c77c9074ad1a6ef6af5f3c75625db9c5be5d552e03bdfb712643fa3262`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Thu, 17 Oct 2024 00:07:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:07:44 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:07:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:07:46 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:09:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:09:05 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7310b1b784f497ecef75a191c3fdf858c6c5e7102326517af7e9c8f4a9ba2ab`  
		Last Modified: Thu, 17 Oct 2024 00:09:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8f60354745986b41d1c97227046f1bf77a40a1b841e2b733d28d9f336d0517a`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81f4ad3b9ee5bb6c5bcf302663adf9404aed5f2a775c97739ddeaf04c390105`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e95309645bd9402810abb1f62e8d28e2eb50ad30d923ac5635718caafc953f3`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1f65e1c7b97054a3ff76d9eb10192f3ffb9f984e554d5dad56b1deffa4a26e`  
		Last Modified: Thu, 17 Oct 2024 00:09:40 GMT  
		Size: 253.1 MB (253069135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3efcc69a49a46842179fb8d2b256e3aca046c05572afb9537e9e68808da649`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11.1` - windows version 10.0.17763.6414; amd64

```console
$ docker pull julia@sha256:5f7b3fa057a3f34c286a0c29544e30b8e25de7d389fcb9a7c39e5dbc2ac59431
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2154909599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73428e1a2c97df8e870d60c63531878514df329661819a1917855fe9c852deb3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Thu, 17 Oct 2024 00:04:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:04:47 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:06:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:06:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4316cb4a890d1430c8dbb6f02f1ed4b07cc1f84668ddfe58d132e70173591231`  
		Last Modified: Thu, 17 Oct 2024 00:06:49 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed07735f2e4d115dbc648a3fbf628ee5e173125dcd63d695a85f30c2d701668d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02cf70042980e2e6296807674462b486e411ba5e80ecf7c6ec3bdd5e0e7a5085`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1c8839b71fde8692b035b2f54ea4a7c21650e10ae20680a0ba68b723b9e57d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4afde2ddc271e774c969b81b72e4ec22aa664487988ca09a851e16930efb47`  
		Last Modified: Thu, 17 Oct 2024 00:07:18 GMT  
		Size: 253.1 MB (253077851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f694e951fd639e6dc35a1e43dce74e5247712830c183397156d8b0ff48747470`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.1-bookworm`

```console
$ docker pull julia@sha256:33cde3f7aaea90daa3bbb93d1a002daf679b68380a9cc24420b90e2c88382d36
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

### `julia:1.11.1-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:fd3a4e95d341cae23b3aef5fcf9fec1d2ee96fd1f1e3bcd6aa64643563ae314f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291937349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ea47312db572c60c8c9351c6b9a422aea6833da9717e5db4e3ea5f32f51b2dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
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
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bb87bd1b2a94a1a42597777f17fe57ac41a63e9ac4631763f29cc1c4eb7971`  
		Last Modified: Thu, 17 Oct 2024 01:21:28 GMT  
		Size: 5.7 MB (5712680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4115daba408d4d475ca265cb576361ce9cf9b002176e4268ae5a0b3eb9853f`  
		Last Modified: Thu, 17 Oct 2024 01:21:36 GMT  
		Size: 257.1 MB (257098011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dff1f91cca18ab23d091ade6d0b0385a0c6050a8fc43fb5a8159e253ae8121b`  
		Last Modified: Thu, 17 Oct 2024 01:21:28 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:57ae5db18ee250b23a45ccc6fdfd5ccfee4d8c87efaf4d1abd057f2769a0329c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2453853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4337eaa6caa92128ea6fc9c7c22d4a311aa67f379c859d92b14a3d50d64a8df7`

```dockerfile
```

-	Layers:
	-	`sha256:63f5d166f6304023b2c389e225252262af1d10b62688335ff269f55508f042ec`  
		Last Modified: Thu, 17 Oct 2024 01:21:28 GMT  
		Size: 2.4 MB (2435621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:065c1f726a44cdf9df5e738e56cd81c29b434fbd47bd7d3361c1137f08dd4cfd`  
		Last Modified: Thu, 17 Oct 2024 01:21:28 GMT  
		Size: 18.2 KB (18232 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.1-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:a2491aa90ba329dafe060d6adb24cb3fb83e36f4c4286633692e583097db3c36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.7 MB (288700700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4129f7f55b30d16e8139c69a813236f23e65139288d9ee0075399d5f6b89e8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
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
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f005b595846e0cdd9b8d61bffb35f19c8e42003b09c6fa5d02f40d76d40d3142`  
		Last Modified: Thu, 17 Oct 2024 13:15:23 GMT  
		Size: 5.5 MB (5537166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c05e13caa8823e23d317536ff1d1dd1796fe2a83847ee02d6db48a22ba0646a`  
		Last Modified: Thu, 17 Oct 2024 13:15:28 GMT  
		Size: 254.0 MB (254006821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a62b6e4f6fa18765799cd22bcbae3f15f20072e9ae053bbdf98a3efe82f52df`  
		Last Modified: Thu, 17 Oct 2024 13:15:23 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:e36e79625d4b2f06ab1b7414a9487e294e789f55949c056a20ab07b607eebe13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2454336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8494e45d3412b161773bf9c522b57e83aa21c819be146fb56574805aae74dfcf`

```dockerfile
```

-	Layers:
	-	`sha256:e348b3b6b5b4e6f22acb995010c94ad138b49e91b49459d7330ea9c665239067`  
		Last Modified: Thu, 17 Oct 2024 13:15:23 GMT  
		Size: 2.4 MB (2435943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f241bd181640f964b873b1a39186238e3c1e3853e6238c3a768fc63f04bd97fc`  
		Last Modified: Thu, 17 Oct 2024 13:15:23 GMT  
		Size: 18.4 KB (18393 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.1-bookworm` - linux; 386

```console
$ docker pull julia@sha256:9664f1d3532459c67196e66b0da1c613348bb1cf1a7dc1c9db5e84315309012c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270672761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e604fb4f328efb8dfd2637df284176512ed1ed6b6c31def9ebcf21aec0c2b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
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
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef46da67fc6417b2c8511177a2f904986a28c82f5f3980c4a3bdda412a0cb96`  
		Last Modified: Thu, 17 Oct 2024 01:21:34 GMT  
		Size: 5.9 MB (5870476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8aa1a2f42b1e06e545c1b61c842a6ba6a571d450dcdddb64e06db764fe22c5c`  
		Last Modified: Thu, 17 Oct 2024 01:21:41 GMT  
		Size: 234.7 MB (234657651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5922d12011579acdb276facae35eb217cd417b8ec2ca21c0b5425fbce9957824`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:5eb0819bd9c824da83af57c0bc587134d66e1189b39e553b460a89a42bdffc69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2450874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4631426bd2f8080a85a75feec2e4cf79652d64624da9905f16d08a1587d6ad79`

```dockerfile
```

-	Layers:
	-	`sha256:fafe3fc46d504391631a308525c4ffbde1b21fc417b2faec508a98df7b15e1ee`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 2.4 MB (2432693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8863f51017c0640fb041800f19fb46fdfab92ec6c3729f6040e84fe38b66c4ed`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 18.2 KB (18181 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.1-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:f1ffa4874e6d100fc1fdce7ae8cff75b4e3cddc3a7063b68467942ab0e7b2d8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.8 MB (283845662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad3f11c30a7d695a2d9d6b9c71b233a341fa06c2f6602447727e3a85aedab3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
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
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ce3688624a92ce5984769ec19a8b421d5cbfdd057e1e30bf5e57cada049215`  
		Last Modified: Thu, 17 Oct 2024 08:42:06 GMT  
		Size: 6.2 MB (6247943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a24702a300837b63b3c298602a67686d45b25deb56363aa065d299c9bdd29b1`  
		Last Modified: Thu, 17 Oct 2024 08:42:14 GMT  
		Size: 244.5 MB (244475147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a582dd71509d2a88c872a94ed8a67e73c053144e9c5664720588c7684748c068`  
		Last Modified: Thu, 17 Oct 2024 08:42:05 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:d6cbf0fa8a4870af9ee3181a941d82be8d58199b70f220a63dd91c918affbbde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2458348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa065e6917f5d7c47bd2416298a0c99812e31e2ddaa68483848ff93690e8f736`

```dockerfile
```

-	Layers:
	-	`sha256:3abe2457e038cfc98e2170b01d92cd1b40f47bfa8cf991cc1220a0da68f000d7`  
		Last Modified: Thu, 17 Oct 2024 08:42:06 GMT  
		Size: 2.4 MB (2440052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4312eae9f6f8c06593b79106a3f06b6ce65b15ecf3c05fce5aba31afba073be7`  
		Last Modified: Thu, 17 Oct 2024 08:42:05 GMT  
		Size: 18.3 KB (18296 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11.1-bullseye`

```console
$ docker pull julia@sha256:d8596315fc3f33f87595593bf6d6c24e7175f1ba2247551b566d73824426057e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.11.1-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:89b0252e81fcee8a8295a302dfbd5333ebf5fc9b2bbcbf21dd0dd432df83bd5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (290953918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c5e3b2a9d92441caccba1899fdfadb95145c7b3454af5d79cc49eef8a2b12dd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
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
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1678fe3cd4a658f476437fee9e77b0c2086786926a90c07b083d0343a3675d34`  
		Last Modified: Thu, 17 Oct 2024 01:21:31 GMT  
		Size: 2.4 MB (2426579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13bf3dac7e14a600162ea26186e3f4f9e2eb67b797a698ca137e9bda78be3095`  
		Last Modified: Thu, 17 Oct 2024 01:21:34 GMT  
		Size: 257.1 MB (257098167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24eeabef1fc4078b2230b57296e3885ca5a8abe902842a963d54dd9229da645`  
		Last Modified: Thu, 17 Oct 2024 01:21:31 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:67cb263e6e9c5a8df2d07f56530084b32aa0fa18b9f54e1c70633d08ee81508f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e7a2b55d44957d73538f15728c85350a58a54b6670423e772b5052af5b609b`

```dockerfile
```

-	Layers:
	-	`sha256:e404b3ce366a6055b639f0e587f8f22d969c64c22ecac08b317416e03980c296`  
		Last Modified: Thu, 17 Oct 2024 01:21:31 GMT  
		Size: 2.7 MB (2703232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1cca66d1ab6aee6b83ad8e00220188da64a51b78924668d3a5d499b22c95b52`  
		Last Modified: Thu, 17 Oct 2024 01:21:31 GMT  
		Size: 17.1 KB (17061 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.1-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4f7f024b62a8f78c7294efa5ae1766b248b3bdf7b9bbb5e9c1416e4e8d1d84fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286497932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e390fcde5664778999f291f06fae01e77921743114fe33fdc45f3115c43c11dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
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
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a413099e7fe61ccf8c3081b040fa09c50cbc6a831480a5614a60a0d3c69b56b8`  
		Last Modified: Thu, 17 Oct 2024 13:16:53 GMT  
		Size: 2.4 MB (2415124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ec42daf214f0d308f8292a6037cc8f045cfdc9adfe28ff544cc0fb9a87b67a`  
		Last Modified: Thu, 17 Oct 2024 13:16:59 GMT  
		Size: 254.0 MB (254006680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a03157b90421e9af495118fb5dd03f42dc3a8de569955b88ad28a1def229884`  
		Last Modified: Thu, 17 Oct 2024 13:16:53 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:37c0ceb7fd6b428c7ce243fdeb9373c1099770d26ebc891187c07606979b3708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d376da6f82e6ccf88c0c94e1cd0081b3dd5ecd7135c4e0a073360dd2f42e4009`

```dockerfile
```

-	Layers:
	-	`sha256:379457b9725569536171521dfa577f8872f6d6231c665f670eb96bc047caa7e1`  
		Last Modified: Thu, 17 Oct 2024 13:16:53 GMT  
		Size: 2.7 MB (2703494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1b312173fb754b10124c5b9d4a848af7c804fd34ba816a297562afe8a0b0353`  
		Last Modified: Thu, 17 Oct 2024 13:16:53 GMT  
		Size: 17.2 KB (17174 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.1-bullseye` - linux; 386

```console
$ docker pull julia@sha256:3670a732c97cffad25985d92fbb803b9b874eca1f6e26a4f56d8a77c91c1deea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.6 MB (269605951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bb8f95ee66c50d9e825aedeb3254da01eaa7c893aec91624b016ac95a35fe7c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD file:05098c6b0b4cfde8b4ffadc861fc7668bbf1779983d50b6be61989e6378fc17b in / 
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
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
	-	`sha256:0aff79075c186716daeb376e46e89131aa14f0dc2bd8f794bd04d72494cb4693`  
		Last Modified: Thu, 17 Oct 2024 00:43:15 GMT  
		Size: 32.4 MB (32413830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351b630321cf786277448e0f7aea94f99fc611feec697422839581d6ba78b0f4`  
		Last Modified: Thu, 17 Oct 2024 01:14:36 GMT  
		Size: 2.5 MB (2533097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a25ec52f239ad17072bdbca92923baca090ca0beb325e15e8b38ec0d9a07bb6`  
		Last Modified: Thu, 17 Oct 2024 01:14:41 GMT  
		Size: 234.7 MB (234658656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacaf77ce79d2cad5f10ebb5c0a2cf0132caef0f18a13b0397f5419a1b104dae`  
		Last Modified: Thu, 17 Oct 2024 01:14:36 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:801107f4fb9fa1d75ece047478ee52a0cde10e3e985cb4235e707647835d9385
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2717361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a242ec47f9cd91c5c05a334d40ffb11921f23481e6fca0e70c18cee75e1be40`

```dockerfile
```

-	Layers:
	-	`sha256:2a3f27893e3c035da08f3858e8b8d9e3d748d8c2d2a8354fba0c038570df9fc1`  
		Last Modified: Thu, 17 Oct 2024 01:14:36 GMT  
		Size: 2.7 MB (2700330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1c148b1faeb4d330bc4cb1657a099ca6c996d5624aa2a62d3c3945b9e70e713`  
		Last Modified: Thu, 17 Oct 2024 01:14:36 GMT  
		Size: 17.0 KB (17031 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11.1-windowsservercore`

```console
$ docker pull julia@sha256:d36dd547370e9fd68c4f5dc635f8c3ea0da809f71f508a8724c909f927574ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `julia:1.11.1-windowsservercore` - windows version 10.0.20348.2762; amd64

```console
$ docker pull julia@sha256:1aadbfaaaab1ead9b289075e1c50a66c24e73f0abb54ff58987658fb3d721339
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2052417149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73d77c77c9074ad1a6ef6af5f3c75625db9c5be5d552e03bdfb712643fa3262`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Thu, 17 Oct 2024 00:07:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:07:44 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:07:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:07:46 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:09:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:09:05 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7310b1b784f497ecef75a191c3fdf858c6c5e7102326517af7e9c8f4a9ba2ab`  
		Last Modified: Thu, 17 Oct 2024 00:09:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8f60354745986b41d1c97227046f1bf77a40a1b841e2b733d28d9f336d0517a`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81f4ad3b9ee5bb6c5bcf302663adf9404aed5f2a775c97739ddeaf04c390105`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e95309645bd9402810abb1f62e8d28e2eb50ad30d923ac5635718caafc953f3`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1f65e1c7b97054a3ff76d9eb10192f3ffb9f984e554d5dad56b1deffa4a26e`  
		Last Modified: Thu, 17 Oct 2024 00:09:40 GMT  
		Size: 253.1 MB (253069135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3efcc69a49a46842179fb8d2b256e3aca046c05572afb9537e9e68808da649`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11.1-windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull julia@sha256:5f7b3fa057a3f34c286a0c29544e30b8e25de7d389fcb9a7c39e5dbc2ac59431
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2154909599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73428e1a2c97df8e870d60c63531878514df329661819a1917855fe9c852deb3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Thu, 17 Oct 2024 00:04:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:04:47 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:06:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:06:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4316cb4a890d1430c8dbb6f02f1ed4b07cc1f84668ddfe58d132e70173591231`  
		Last Modified: Thu, 17 Oct 2024 00:06:49 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed07735f2e4d115dbc648a3fbf628ee5e173125dcd63d695a85f30c2d701668d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02cf70042980e2e6296807674462b486e411ba5e80ecf7c6ec3bdd5e0e7a5085`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1c8839b71fde8692b035b2f54ea4a7c21650e10ae20680a0ba68b723b9e57d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4afde2ddc271e774c969b81b72e4ec22aa664487988ca09a851e16930efb47`  
		Last Modified: Thu, 17 Oct 2024 00:07:18 GMT  
		Size: 253.1 MB (253077851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f694e951fd639e6dc35a1e43dce74e5247712830c183397156d8b0ff48747470`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.1-windowsservercore-1809`

```console
$ docker pull julia@sha256:a114dd8364b3c4135706a0b323f71e0e649bff9cf95ae8300f0378d0951c131e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `julia:1.11.1-windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull julia@sha256:5f7b3fa057a3f34c286a0c29544e30b8e25de7d389fcb9a7c39e5dbc2ac59431
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2154909599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73428e1a2c97df8e870d60c63531878514df329661819a1917855fe9c852deb3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Thu, 17 Oct 2024 00:04:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:04:47 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:06:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:06:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4316cb4a890d1430c8dbb6f02f1ed4b07cc1f84668ddfe58d132e70173591231`  
		Last Modified: Thu, 17 Oct 2024 00:06:49 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed07735f2e4d115dbc648a3fbf628ee5e173125dcd63d695a85f30c2d701668d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02cf70042980e2e6296807674462b486e411ba5e80ecf7c6ec3bdd5e0e7a5085`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1c8839b71fde8692b035b2f54ea4a7c21650e10ae20680a0ba68b723b9e57d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4afde2ddc271e774c969b81b72e4ec22aa664487988ca09a851e16930efb47`  
		Last Modified: Thu, 17 Oct 2024 00:07:18 GMT  
		Size: 253.1 MB (253077851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f694e951fd639e6dc35a1e43dce74e5247712830c183397156d8b0ff48747470`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:e457f763ca8c5fe3e8a20dd1a3cbf00134231b70f5070b6fa7ce67ff9536e8dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `julia:1.11.1-windowsservercore-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull julia@sha256:1aadbfaaaab1ead9b289075e1c50a66c24e73f0abb54ff58987658fb3d721339
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2052417149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73d77c77c9074ad1a6ef6af5f3c75625db9c5be5d552e03bdfb712643fa3262`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Thu, 17 Oct 2024 00:07:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:07:44 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:07:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:07:46 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:09:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:09:05 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7310b1b784f497ecef75a191c3fdf858c6c5e7102326517af7e9c8f4a9ba2ab`  
		Last Modified: Thu, 17 Oct 2024 00:09:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8f60354745986b41d1c97227046f1bf77a40a1b841e2b733d28d9f336d0517a`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81f4ad3b9ee5bb6c5bcf302663adf9404aed5f2a775c97739ddeaf04c390105`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e95309645bd9402810abb1f62e8d28e2eb50ad30d923ac5635718caafc953f3`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1f65e1c7b97054a3ff76d9eb10192f3ffb9f984e554d5dad56b1deffa4a26e`  
		Last Modified: Thu, 17 Oct 2024 00:09:40 GMT  
		Size: 253.1 MB (253069135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3efcc69a49a46842179fb8d2b256e3aca046c05572afb9537e9e68808da649`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:bookworm`

```console
$ docker pull julia@sha256:33cde3f7aaea90daa3bbb93d1a002daf679b68380a9cc24420b90e2c88382d36
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
$ docker pull julia@sha256:fd3a4e95d341cae23b3aef5fcf9fec1d2ee96fd1f1e3bcd6aa64643563ae314f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291937349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ea47312db572c60c8c9351c6b9a422aea6833da9717e5db4e3ea5f32f51b2dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
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
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bb87bd1b2a94a1a42597777f17fe57ac41a63e9ac4631763f29cc1c4eb7971`  
		Last Modified: Thu, 17 Oct 2024 01:21:28 GMT  
		Size: 5.7 MB (5712680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4115daba408d4d475ca265cb576361ce9cf9b002176e4268ae5a0b3eb9853f`  
		Last Modified: Thu, 17 Oct 2024 01:21:36 GMT  
		Size: 257.1 MB (257098011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dff1f91cca18ab23d091ade6d0b0385a0c6050a8fc43fb5a8159e253ae8121b`  
		Last Modified: Thu, 17 Oct 2024 01:21:28 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:57ae5db18ee250b23a45ccc6fdfd5ccfee4d8c87efaf4d1abd057f2769a0329c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2453853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4337eaa6caa92128ea6fc9c7c22d4a311aa67f379c859d92b14a3d50d64a8df7`

```dockerfile
```

-	Layers:
	-	`sha256:63f5d166f6304023b2c389e225252262af1d10b62688335ff269f55508f042ec`  
		Last Modified: Thu, 17 Oct 2024 01:21:28 GMT  
		Size: 2.4 MB (2435621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:065c1f726a44cdf9df5e738e56cd81c29b434fbd47bd7d3361c1137f08dd4cfd`  
		Last Modified: Thu, 17 Oct 2024 01:21:28 GMT  
		Size: 18.2 KB (18232 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:a2491aa90ba329dafe060d6adb24cb3fb83e36f4c4286633692e583097db3c36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.7 MB (288700700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4129f7f55b30d16e8139c69a813236f23e65139288d9ee0075399d5f6b89e8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
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
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f005b595846e0cdd9b8d61bffb35f19c8e42003b09c6fa5d02f40d76d40d3142`  
		Last Modified: Thu, 17 Oct 2024 13:15:23 GMT  
		Size: 5.5 MB (5537166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c05e13caa8823e23d317536ff1d1dd1796fe2a83847ee02d6db48a22ba0646a`  
		Last Modified: Thu, 17 Oct 2024 13:15:28 GMT  
		Size: 254.0 MB (254006821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a62b6e4f6fa18765799cd22bcbae3f15f20072e9ae053bbdf98a3efe82f52df`  
		Last Modified: Thu, 17 Oct 2024 13:15:23 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:e36e79625d4b2f06ab1b7414a9487e294e789f55949c056a20ab07b607eebe13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2454336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8494e45d3412b161773bf9c522b57e83aa21c819be146fb56574805aae74dfcf`

```dockerfile
```

-	Layers:
	-	`sha256:e348b3b6b5b4e6f22acb995010c94ad138b49e91b49459d7330ea9c665239067`  
		Last Modified: Thu, 17 Oct 2024 13:15:23 GMT  
		Size: 2.4 MB (2435943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f241bd181640f964b873b1a39186238e3c1e3853e6238c3a768fc63f04bd97fc`  
		Last Modified: Thu, 17 Oct 2024 13:15:23 GMT  
		Size: 18.4 KB (18393 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; 386

```console
$ docker pull julia@sha256:9664f1d3532459c67196e66b0da1c613348bb1cf1a7dc1c9db5e84315309012c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270672761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e604fb4f328efb8dfd2637df284176512ed1ed6b6c31def9ebcf21aec0c2b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
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
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef46da67fc6417b2c8511177a2f904986a28c82f5f3980c4a3bdda412a0cb96`  
		Last Modified: Thu, 17 Oct 2024 01:21:34 GMT  
		Size: 5.9 MB (5870476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8aa1a2f42b1e06e545c1b61c842a6ba6a571d450dcdddb64e06db764fe22c5c`  
		Last Modified: Thu, 17 Oct 2024 01:21:41 GMT  
		Size: 234.7 MB (234657651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5922d12011579acdb276facae35eb217cd417b8ec2ca21c0b5425fbce9957824`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:5eb0819bd9c824da83af57c0bc587134d66e1189b39e553b460a89a42bdffc69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2450874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4631426bd2f8080a85a75feec2e4cf79652d64624da9905f16d08a1587d6ad79`

```dockerfile
```

-	Layers:
	-	`sha256:fafe3fc46d504391631a308525c4ffbde1b21fc417b2faec508a98df7b15e1ee`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 2.4 MB (2432693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8863f51017c0640fb041800f19fb46fdfab92ec6c3729f6040e84fe38b66c4ed`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 18.2 KB (18181 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:f1ffa4874e6d100fc1fdce7ae8cff75b4e3cddc3a7063b68467942ab0e7b2d8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.8 MB (283845662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad3f11c30a7d695a2d9d6b9c71b233a341fa06c2f6602447727e3a85aedab3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
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
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ce3688624a92ce5984769ec19a8b421d5cbfdd057e1e30bf5e57cada049215`  
		Last Modified: Thu, 17 Oct 2024 08:42:06 GMT  
		Size: 6.2 MB (6247943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a24702a300837b63b3c298602a67686d45b25deb56363aa065d299c9bdd29b1`  
		Last Modified: Thu, 17 Oct 2024 08:42:14 GMT  
		Size: 244.5 MB (244475147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a582dd71509d2a88c872a94ed8a67e73c053144e9c5664720588c7684748c068`  
		Last Modified: Thu, 17 Oct 2024 08:42:05 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:d6cbf0fa8a4870af9ee3181a941d82be8d58199b70f220a63dd91c918affbbde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2458348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa065e6917f5d7c47bd2416298a0c99812e31e2ddaa68483848ff93690e8f736`

```dockerfile
```

-	Layers:
	-	`sha256:3abe2457e038cfc98e2170b01d92cd1b40f47bfa8cf991cc1220a0da68f000d7`  
		Last Modified: Thu, 17 Oct 2024 08:42:06 GMT  
		Size: 2.4 MB (2440052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4312eae9f6f8c06593b79106a3f06b6ce65b15ecf3c05fce5aba31afba073be7`  
		Last Modified: Thu, 17 Oct 2024 08:42:05 GMT  
		Size: 18.3 KB (18296 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:bullseye`

```console
$ docker pull julia@sha256:d8596315fc3f33f87595593bf6d6c24e7175f1ba2247551b566d73824426057e
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
$ docker pull julia@sha256:89b0252e81fcee8a8295a302dfbd5333ebf5fc9b2bbcbf21dd0dd432df83bd5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (290953918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c5e3b2a9d92441caccba1899fdfadb95145c7b3454af5d79cc49eef8a2b12dd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
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
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1678fe3cd4a658f476437fee9e77b0c2086786926a90c07b083d0343a3675d34`  
		Last Modified: Thu, 17 Oct 2024 01:21:31 GMT  
		Size: 2.4 MB (2426579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13bf3dac7e14a600162ea26186e3f4f9e2eb67b797a698ca137e9bda78be3095`  
		Last Modified: Thu, 17 Oct 2024 01:21:34 GMT  
		Size: 257.1 MB (257098167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24eeabef1fc4078b2230b57296e3885ca5a8abe902842a963d54dd9229da645`  
		Last Modified: Thu, 17 Oct 2024 01:21:31 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:67cb263e6e9c5a8df2d07f56530084b32aa0fa18b9f54e1c70633d08ee81508f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e7a2b55d44957d73538f15728c85350a58a54b6670423e772b5052af5b609b`

```dockerfile
```

-	Layers:
	-	`sha256:e404b3ce366a6055b639f0e587f8f22d969c64c22ecac08b317416e03980c296`  
		Last Modified: Thu, 17 Oct 2024 01:21:31 GMT  
		Size: 2.7 MB (2703232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1cca66d1ab6aee6b83ad8e00220188da64a51b78924668d3a5d499b22c95b52`  
		Last Modified: Thu, 17 Oct 2024 01:21:31 GMT  
		Size: 17.1 KB (17061 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4f7f024b62a8f78c7294efa5ae1766b248b3bdf7b9bbb5e9c1416e4e8d1d84fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286497932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e390fcde5664778999f291f06fae01e77921743114fe33fdc45f3115c43c11dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
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
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a413099e7fe61ccf8c3081b040fa09c50cbc6a831480a5614a60a0d3c69b56b8`  
		Last Modified: Thu, 17 Oct 2024 13:16:53 GMT  
		Size: 2.4 MB (2415124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ec42daf214f0d308f8292a6037cc8f045cfdc9adfe28ff544cc0fb9a87b67a`  
		Last Modified: Thu, 17 Oct 2024 13:16:59 GMT  
		Size: 254.0 MB (254006680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a03157b90421e9af495118fb5dd03f42dc3a8de569955b88ad28a1def229884`  
		Last Modified: Thu, 17 Oct 2024 13:16:53 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:37c0ceb7fd6b428c7ce243fdeb9373c1099770d26ebc891187c07606979b3708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d376da6f82e6ccf88c0c94e1cd0081b3dd5ecd7135c4e0a073360dd2f42e4009`

```dockerfile
```

-	Layers:
	-	`sha256:379457b9725569536171521dfa577f8872f6d6231c665f670eb96bc047caa7e1`  
		Last Modified: Thu, 17 Oct 2024 13:16:53 GMT  
		Size: 2.7 MB (2703494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1b312173fb754b10124c5b9d4a848af7c804fd34ba816a297562afe8a0b0353`  
		Last Modified: Thu, 17 Oct 2024 13:16:53 GMT  
		Size: 17.2 KB (17174 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bullseye` - linux; 386

```console
$ docker pull julia@sha256:3670a732c97cffad25985d92fbb803b9b874eca1f6e26a4f56d8a77c91c1deea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.6 MB (269605951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bb8f95ee66c50d9e825aedeb3254da01eaa7c893aec91624b016ac95a35fe7c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD file:05098c6b0b4cfde8b4ffadc861fc7668bbf1779983d50b6be61989e6378fc17b in / 
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
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
	-	`sha256:0aff79075c186716daeb376e46e89131aa14f0dc2bd8f794bd04d72494cb4693`  
		Last Modified: Thu, 17 Oct 2024 00:43:15 GMT  
		Size: 32.4 MB (32413830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351b630321cf786277448e0f7aea94f99fc611feec697422839581d6ba78b0f4`  
		Last Modified: Thu, 17 Oct 2024 01:14:36 GMT  
		Size: 2.5 MB (2533097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a25ec52f239ad17072bdbca92923baca090ca0beb325e15e8b38ec0d9a07bb6`  
		Last Modified: Thu, 17 Oct 2024 01:14:41 GMT  
		Size: 234.7 MB (234658656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacaf77ce79d2cad5f10ebb5c0a2cf0132caef0f18a13b0397f5419a1b104dae`  
		Last Modified: Thu, 17 Oct 2024 01:14:36 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:801107f4fb9fa1d75ece047478ee52a0cde10e3e985cb4235e707647835d9385
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2717361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a242ec47f9cd91c5c05a334d40ffb11921f23481e6fca0e70c18cee75e1be40`

```dockerfile
```

-	Layers:
	-	`sha256:2a3f27893e3c035da08f3858e8b8d9e3d748d8c2d2a8354fba0c038570df9fc1`  
		Last Modified: Thu, 17 Oct 2024 01:14:36 GMT  
		Size: 2.7 MB (2700330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1c148b1faeb4d330bc4cb1657a099ca6c996d5624aa2a62d3c3945b9e70e713`  
		Last Modified: Thu, 17 Oct 2024 01:14:36 GMT  
		Size: 17.0 KB (17031 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:latest`

```console
$ docker pull julia@sha256:59ccf7b59abf7f7d78813b5fb0e244b0c7830c5656b956f9fde7bd27626476c0
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
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `julia:latest` - linux; amd64

```console
$ docker pull julia@sha256:fd3a4e95d341cae23b3aef5fcf9fec1d2ee96fd1f1e3bcd6aa64643563ae314f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291937349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ea47312db572c60c8c9351c6b9a422aea6833da9717e5db4e3ea5f32f51b2dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
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
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bb87bd1b2a94a1a42597777f17fe57ac41a63e9ac4631763f29cc1c4eb7971`  
		Last Modified: Thu, 17 Oct 2024 01:21:28 GMT  
		Size: 5.7 MB (5712680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4115daba408d4d475ca265cb576361ce9cf9b002176e4268ae5a0b3eb9853f`  
		Last Modified: Thu, 17 Oct 2024 01:21:36 GMT  
		Size: 257.1 MB (257098011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dff1f91cca18ab23d091ade6d0b0385a0c6050a8fc43fb5a8159e253ae8121b`  
		Last Modified: Thu, 17 Oct 2024 01:21:28 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:57ae5db18ee250b23a45ccc6fdfd5ccfee4d8c87efaf4d1abd057f2769a0329c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2453853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4337eaa6caa92128ea6fc9c7c22d4a311aa67f379c859d92b14a3d50d64a8df7`

```dockerfile
```

-	Layers:
	-	`sha256:63f5d166f6304023b2c389e225252262af1d10b62688335ff269f55508f042ec`  
		Last Modified: Thu, 17 Oct 2024 01:21:28 GMT  
		Size: 2.4 MB (2435621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:065c1f726a44cdf9df5e738e56cd81c29b434fbd47bd7d3361c1137f08dd4cfd`  
		Last Modified: Thu, 17 Oct 2024 01:21:28 GMT  
		Size: 18.2 KB (18232 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:a2491aa90ba329dafe060d6adb24cb3fb83e36f4c4286633692e583097db3c36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.7 MB (288700700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4129f7f55b30d16e8139c69a813236f23e65139288d9ee0075399d5f6b89e8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
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
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f005b595846e0cdd9b8d61bffb35f19c8e42003b09c6fa5d02f40d76d40d3142`  
		Last Modified: Thu, 17 Oct 2024 13:15:23 GMT  
		Size: 5.5 MB (5537166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c05e13caa8823e23d317536ff1d1dd1796fe2a83847ee02d6db48a22ba0646a`  
		Last Modified: Thu, 17 Oct 2024 13:15:28 GMT  
		Size: 254.0 MB (254006821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a62b6e4f6fa18765799cd22bcbae3f15f20072e9ae053bbdf98a3efe82f52df`  
		Last Modified: Thu, 17 Oct 2024 13:15:23 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:e36e79625d4b2f06ab1b7414a9487e294e789f55949c056a20ab07b607eebe13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2454336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8494e45d3412b161773bf9c522b57e83aa21c819be146fb56574805aae74dfcf`

```dockerfile
```

-	Layers:
	-	`sha256:e348b3b6b5b4e6f22acb995010c94ad138b49e91b49459d7330ea9c665239067`  
		Last Modified: Thu, 17 Oct 2024 13:15:23 GMT  
		Size: 2.4 MB (2435943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f241bd181640f964b873b1a39186238e3c1e3853e6238c3a768fc63f04bd97fc`  
		Last Modified: Thu, 17 Oct 2024 13:15:23 GMT  
		Size: 18.4 KB (18393 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; 386

```console
$ docker pull julia@sha256:9664f1d3532459c67196e66b0da1c613348bb1cf1a7dc1c9db5e84315309012c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270672761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e604fb4f328efb8dfd2637df284176512ed1ed6b6c31def9ebcf21aec0c2b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
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
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef46da67fc6417b2c8511177a2f904986a28c82f5f3980c4a3bdda412a0cb96`  
		Last Modified: Thu, 17 Oct 2024 01:21:34 GMT  
		Size: 5.9 MB (5870476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8aa1a2f42b1e06e545c1b61c842a6ba6a571d450dcdddb64e06db764fe22c5c`  
		Last Modified: Thu, 17 Oct 2024 01:21:41 GMT  
		Size: 234.7 MB (234657651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5922d12011579acdb276facae35eb217cd417b8ec2ca21c0b5425fbce9957824`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:5eb0819bd9c824da83af57c0bc587134d66e1189b39e553b460a89a42bdffc69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2450874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4631426bd2f8080a85a75feec2e4cf79652d64624da9905f16d08a1587d6ad79`

```dockerfile
```

-	Layers:
	-	`sha256:fafe3fc46d504391631a308525c4ffbde1b21fc417b2faec508a98df7b15e1ee`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 2.4 MB (2432693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8863f51017c0640fb041800f19fb46fdfab92ec6c3729f6040e84fe38b66c4ed`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 18.2 KB (18181 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; ppc64le

```console
$ docker pull julia@sha256:f1ffa4874e6d100fc1fdce7ae8cff75b4e3cddc3a7063b68467942ab0e7b2d8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.8 MB (283845662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad3f11c30a7d695a2d9d6b9c71b233a341fa06c2f6602447727e3a85aedab3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
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
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ce3688624a92ce5984769ec19a8b421d5cbfdd057e1e30bf5e57cada049215`  
		Last Modified: Thu, 17 Oct 2024 08:42:06 GMT  
		Size: 6.2 MB (6247943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a24702a300837b63b3c298602a67686d45b25deb56363aa065d299c9bdd29b1`  
		Last Modified: Thu, 17 Oct 2024 08:42:14 GMT  
		Size: 244.5 MB (244475147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a582dd71509d2a88c872a94ed8a67e73c053144e9c5664720588c7684748c068`  
		Last Modified: Thu, 17 Oct 2024 08:42:05 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:d6cbf0fa8a4870af9ee3181a941d82be8d58199b70f220a63dd91c918affbbde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2458348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa065e6917f5d7c47bd2416298a0c99812e31e2ddaa68483848ff93690e8f736`

```dockerfile
```

-	Layers:
	-	`sha256:3abe2457e038cfc98e2170b01d92cd1b40f47bfa8cf991cc1220a0da68f000d7`  
		Last Modified: Thu, 17 Oct 2024 08:42:06 GMT  
		Size: 2.4 MB (2440052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4312eae9f6f8c06593b79106a3f06b6ce65b15ecf3c05fce5aba31afba073be7`  
		Last Modified: Thu, 17 Oct 2024 08:42:05 GMT  
		Size: 18.3 KB (18296 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - windows version 10.0.20348.2762; amd64

```console
$ docker pull julia@sha256:1aadbfaaaab1ead9b289075e1c50a66c24e73f0abb54ff58987658fb3d721339
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2052417149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73d77c77c9074ad1a6ef6af5f3c75625db9c5be5d552e03bdfb712643fa3262`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Thu, 17 Oct 2024 00:07:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:07:44 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:07:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:07:46 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:09:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:09:05 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7310b1b784f497ecef75a191c3fdf858c6c5e7102326517af7e9c8f4a9ba2ab`  
		Last Modified: Thu, 17 Oct 2024 00:09:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8f60354745986b41d1c97227046f1bf77a40a1b841e2b733d28d9f336d0517a`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81f4ad3b9ee5bb6c5bcf302663adf9404aed5f2a775c97739ddeaf04c390105`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e95309645bd9402810abb1f62e8d28e2eb50ad30d923ac5635718caafc953f3`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1f65e1c7b97054a3ff76d9eb10192f3ffb9f984e554d5dad56b1deffa4a26e`  
		Last Modified: Thu, 17 Oct 2024 00:09:40 GMT  
		Size: 253.1 MB (253069135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3efcc69a49a46842179fb8d2b256e3aca046c05572afb9537e9e68808da649`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.17763.6414; amd64

```console
$ docker pull julia@sha256:5f7b3fa057a3f34c286a0c29544e30b8e25de7d389fcb9a7c39e5dbc2ac59431
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2154909599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73428e1a2c97df8e870d60c63531878514df329661819a1917855fe9c852deb3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Thu, 17 Oct 2024 00:04:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:04:47 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:06:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:06:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4316cb4a890d1430c8dbb6f02f1ed4b07cc1f84668ddfe58d132e70173591231`  
		Last Modified: Thu, 17 Oct 2024 00:06:49 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed07735f2e4d115dbc648a3fbf628ee5e173125dcd63d695a85f30c2d701668d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02cf70042980e2e6296807674462b486e411ba5e80ecf7c6ec3bdd5e0e7a5085`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1c8839b71fde8692b035b2f54ea4a7c21650e10ae20680a0ba68b723b9e57d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4afde2ddc271e774c969b81b72e4ec22aa664487988ca09a851e16930efb47`  
		Last Modified: Thu, 17 Oct 2024 00:07:18 GMT  
		Size: 253.1 MB (253077851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f694e951fd639e6dc35a1e43dce74e5247712830c183397156d8b0ff48747470`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore`

```console
$ docker pull julia@sha256:d36dd547370e9fd68c4f5dc635f8c3ea0da809f71f508a8724c909f927574ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `julia:windowsservercore` - windows version 10.0.20348.2762; amd64

```console
$ docker pull julia@sha256:1aadbfaaaab1ead9b289075e1c50a66c24e73f0abb54ff58987658fb3d721339
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2052417149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73d77c77c9074ad1a6ef6af5f3c75625db9c5be5d552e03bdfb712643fa3262`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Thu, 17 Oct 2024 00:07:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:07:44 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:07:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:07:46 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:09:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:09:05 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7310b1b784f497ecef75a191c3fdf858c6c5e7102326517af7e9c8f4a9ba2ab`  
		Last Modified: Thu, 17 Oct 2024 00:09:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8f60354745986b41d1c97227046f1bf77a40a1b841e2b733d28d9f336d0517a`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81f4ad3b9ee5bb6c5bcf302663adf9404aed5f2a775c97739ddeaf04c390105`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e95309645bd9402810abb1f62e8d28e2eb50ad30d923ac5635718caafc953f3`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1f65e1c7b97054a3ff76d9eb10192f3ffb9f984e554d5dad56b1deffa4a26e`  
		Last Modified: Thu, 17 Oct 2024 00:09:40 GMT  
		Size: 253.1 MB (253069135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3efcc69a49a46842179fb8d2b256e3aca046c05572afb9537e9e68808da649`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull julia@sha256:5f7b3fa057a3f34c286a0c29544e30b8e25de7d389fcb9a7c39e5dbc2ac59431
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2154909599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73428e1a2c97df8e870d60c63531878514df329661819a1917855fe9c852deb3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Thu, 17 Oct 2024 00:04:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:04:47 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:06:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:06:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4316cb4a890d1430c8dbb6f02f1ed4b07cc1f84668ddfe58d132e70173591231`  
		Last Modified: Thu, 17 Oct 2024 00:06:49 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed07735f2e4d115dbc648a3fbf628ee5e173125dcd63d695a85f30c2d701668d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02cf70042980e2e6296807674462b486e411ba5e80ecf7c6ec3bdd5e0e7a5085`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1c8839b71fde8692b035b2f54ea4a7c21650e10ae20680a0ba68b723b9e57d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4afde2ddc271e774c969b81b72e4ec22aa664487988ca09a851e16930efb47`  
		Last Modified: Thu, 17 Oct 2024 00:07:18 GMT  
		Size: 253.1 MB (253077851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f694e951fd639e6dc35a1e43dce74e5247712830c183397156d8b0ff48747470`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore-1809`

```console
$ docker pull julia@sha256:a114dd8364b3c4135706a0b323f71e0e649bff9cf95ae8300f0378d0951c131e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `julia:windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull julia@sha256:5f7b3fa057a3f34c286a0c29544e30b8e25de7d389fcb9a7c39e5dbc2ac59431
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2154909599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73428e1a2c97df8e870d60c63531878514df329661819a1917855fe9c852deb3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Thu, 17 Oct 2024 00:04:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:04:47 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:06:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:06:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4316cb4a890d1430c8dbb6f02f1ed4b07cc1f84668ddfe58d132e70173591231`  
		Last Modified: Thu, 17 Oct 2024 00:06:49 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed07735f2e4d115dbc648a3fbf628ee5e173125dcd63d695a85f30c2d701668d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02cf70042980e2e6296807674462b486e411ba5e80ecf7c6ec3bdd5e0e7a5085`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1c8839b71fde8692b035b2f54ea4a7c21650e10ae20680a0ba68b723b9e57d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4afde2ddc271e774c969b81b72e4ec22aa664487988ca09a851e16930efb47`  
		Last Modified: Thu, 17 Oct 2024 00:07:18 GMT  
		Size: 253.1 MB (253077851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f694e951fd639e6dc35a1e43dce74e5247712830c183397156d8b0ff48747470`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:e457f763ca8c5fe3e8a20dd1a3cbf00134231b70f5070b6fa7ce67ff9536e8dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `julia:windowsservercore-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull julia@sha256:1aadbfaaaab1ead9b289075e1c50a66c24e73f0abb54ff58987658fb3d721339
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2052417149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73d77c77c9074ad1a6ef6af5f3c75625db9c5be5d552e03bdfb712643fa3262`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Thu, 17 Oct 2024 00:07:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:07:44 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:07:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:07:46 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:09:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:09:05 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7310b1b784f497ecef75a191c3fdf858c6c5e7102326517af7e9c8f4a9ba2ab`  
		Last Modified: Thu, 17 Oct 2024 00:09:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8f60354745986b41d1c97227046f1bf77a40a1b841e2b733d28d9f336d0517a`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81f4ad3b9ee5bb6c5bcf302663adf9404aed5f2a775c97739ddeaf04c390105`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e95309645bd9402810abb1f62e8d28e2eb50ad30d923ac5635718caafc953f3`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1f65e1c7b97054a3ff76d9eb10192f3ffb9f984e554d5dad56b1deffa4a26e`  
		Last Modified: Thu, 17 Oct 2024 00:09:40 GMT  
		Size: 253.1 MB (253069135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3efcc69a49a46842179fb8d2b256e3aca046c05572afb9537e9e68808da649`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
