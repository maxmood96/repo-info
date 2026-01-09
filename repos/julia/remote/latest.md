## `julia:latest`

```console
$ docker pull julia@sha256:2749295df1d9d05ac818a71b13462f38370ba01ff7ba0551b21bc57439d1412b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.26100.7462; amd64
	-	windows version 10.0.20348.4529; amd64

### `julia:latest` - linux; amd64

```console
$ docker pull julia@sha256:e3b9aae4eb2355b283a6ddcbae81164e0322184b273dd6795e41244611ff86d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.9 MB (325875226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:770e08b4a184be6ec8f6a7efea76904cf57d1ae9ffb41e6e32cf1eb4e91245ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Thu, 08 Jan 2026 19:02:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Jan 2026 19:03:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 08 Jan 2026 19:03:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Jan 2026 19:03:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 08 Jan 2026 19:03:18 GMT
ENV JULIA_VERSION=1.12.4
# Thu, 08 Jan 2026 19:03:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.4-linux-x86_64.tar.gz'; 			sha256='c57baf178fe140926acb1a25396d482f325af9d7908d9b066d2fbc0d6639985d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.4-linux-i686.tar.gz'; 			sha256='fb7c91de825ecd6bc3d9960e9fc18c44052e82bcb4a5d2f626e6932de5f34968'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.4-linux-aarch64.tar.gz'; 			sha256='a602a2dfee931224fd68e47567dc672743e2fd9e80f39d84cf3c99afc9663ddd'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 08 Jan 2026 19:03:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 08 Jan 2026 19:03:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Jan 2026 19:03:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ddf41fe75fc74205732f8081c24808de2e1cc6214bbd46afbb11f59a9da06e`  
		Last Modified: Thu, 08 Jan 2026 19:04:28 GMT  
		Size: 6.2 MB (6242897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a8398e79424aeddb06ebb499555863dcc529dafd74c10d98747c776f858a0a`  
		Last Modified: Thu, 08 Jan 2026 19:04:53 GMT  
		Size: 289.9 MB (289855424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef12a58cc89dc81313968f11025c9a62710dd2cb282f855e745294ca688d8d65`  
		Last Modified: Thu, 08 Jan 2026 19:04:27 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:99ff53154ba22195a6c3236a50866319e21f4e31dcbce5403e6588bb52c56c6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc2351214cb6f1d7d9db346ef80e081c84ad6db3376f85278ee1f2197854de4b`

```dockerfile
```

-	Layers:
	-	`sha256:e376aec5d1df7c6b98a69425656e51ac5f4be9f955525d2eedac6f0d230a96c3`  
		Last Modified: Thu, 08 Jan 2026 21:02:52 GMT  
		Size: 2.2 MB (2240123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6682220f478b137da8016516d512db68958f822e15dc1aa35fe094205532afa1`  
		Last Modified: Thu, 08 Jan 2026 21:02:53 GMT  
		Size: 17.7 KB (17689 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:0b6f7d11b3b0b711cbdade209d4430723fde3a0a1ad0de7bbe1269ff90b7b1b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.6 MB (347590011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d00b3b1d84876dd7b649430add81a78a6aff6657230a5e26d003cf58101653a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Thu, 08 Jan 2026 19:02:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Jan 2026 19:03:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 08 Jan 2026 19:03:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Jan 2026 19:03:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 08 Jan 2026 19:03:19 GMT
ENV JULIA_VERSION=1.12.4
# Thu, 08 Jan 2026 19:03:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.4-linux-x86_64.tar.gz'; 			sha256='c57baf178fe140926acb1a25396d482f325af9d7908d9b066d2fbc0d6639985d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.4-linux-i686.tar.gz'; 			sha256='fb7c91de825ecd6bc3d9960e9fc18c44052e82bcb4a5d2f626e6932de5f34968'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.4-linux-aarch64.tar.gz'; 			sha256='a602a2dfee931224fd68e47567dc672743e2fd9e80f39d84cf3c99afc9663ddd'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 08 Jan 2026 19:03:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 08 Jan 2026 19:03:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Jan 2026 19:03:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce7a00eb39fa2cf8464c153e30dd9a14f68255fd1585bfd0098048d4959eea8`  
		Last Modified: Thu, 08 Jan 2026 19:04:30 GMT  
		Size: 6.2 MB (6153397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7761f992c74d29e5e78308bd920eaad02407c55dffaee75d254aa777caabe2`  
		Last Modified: Thu, 08 Jan 2026 19:05:14 GMT  
		Size: 311.3 MB (311297609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41fe9f76d00cfc4c430901b8627695a7300aa07e9d9c01d951a77303a408383`  
		Last Modified: Thu, 08 Jan 2026 19:04:30 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:ffd0054c63388efeca699bca0295896886aea694f933067c351c770bfd81639a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17f234e7bd2d5198bdcee7ef074d808712a71ee3d95e1bcefbb94a7538fd8f69`

```dockerfile
```

-	Layers:
	-	`sha256:1ce4e3fa471062ec2c789a0dac7d1b211eaf97d5149e216387ab21ca003b1644`  
		Last Modified: Thu, 08 Jan 2026 21:02:57 GMT  
		Size: 2.2 MB (2240455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:178b5235d50e7581da6e19501ab38fd0929e39a1468c9f21c22e9a5f5c4e13a6`  
		Last Modified: Thu, 08 Jan 2026 21:02:58 GMT  
		Size: 17.9 KB (17856 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; 386

```console
$ docker pull julia@sha256:47f498e5b8b277971dd78af7f61e2ec7336b227726af9af29049e8e1b0f3e467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268967675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13fc57974276760254a049f97d518405bd8fdd6a195c906d9b53d86a03a47d9e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1766966400'
# Thu, 08 Jan 2026 19:02:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Jan 2026 19:03:22 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 08 Jan 2026 19:03:22 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Jan 2026 19:03:22 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 08 Jan 2026 19:03:22 GMT
ENV JULIA_VERSION=1.12.4
# Thu, 08 Jan 2026 19:03:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.4-linux-x86_64.tar.gz'; 			sha256='c57baf178fe140926acb1a25396d482f325af9d7908d9b066d2fbc0d6639985d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.4-linux-i686.tar.gz'; 			sha256='fb7c91de825ecd6bc3d9960e9fc18c44052e82bcb4a5d2f626e6932de5f34968'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.4-linux-aarch64.tar.gz'; 			sha256='a602a2dfee931224fd68e47567dc672743e2fd9e80f39d84cf3c99afc9663ddd'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 08 Jan 2026 19:03:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 08 Jan 2026 19:03:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Jan 2026 19:03:22 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:796ffff142a3158a5c48a8d81b8b722c5cf4889d5e22da70bdd13a6459d6e40b`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 31.3 MB (31293100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec842386bb3af8b658bf1f7cc4abf1ab851ec517b372704749d458433e6aa48`  
		Last Modified: Thu, 08 Jan 2026 19:04:17 GMT  
		Size: 6.4 MB (6427650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eedec7cf597963356c73abdeaa0e7317584bbb4c0132d709273f57401fa694d`  
		Last Modified: Thu, 08 Jan 2026 19:05:39 GMT  
		Size: 231.2 MB (231246557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee67f188a5634c04590de1ce4d3b6efe17b37c8e6db92b7cae4d6d9b2b69b126`  
		Last Modified: Thu, 08 Jan 2026 19:04:17 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:b5a0a9578eca053cba917a786cb5f42f87cc734eecd136e34f8db21d0258d823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a4626b951fde2db628c7f6d7f98d331885136835e5fdcd5dbff198d31c421fc`

```dockerfile
```

-	Layers:
	-	`sha256:dc40b58e9051178a4b72e922d4e46018be304aab1540182e1f061474130a09b3`  
		Last Modified: Thu, 08 Jan 2026 21:03:02 GMT  
		Size: 2.2 MB (2237248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0635574a99c872f1a1bbb7a5c2889986ece6b175181aad003939aedffb35a412`  
		Last Modified: Thu, 08 Jan 2026 21:03:03 GMT  
		Size: 17.6 KB (17635 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - windows version 10.0.26100.7462; amd64

```console
$ docker pull julia@sha256:3812efd7cda1f33f17589be8fed11480dde73ffb2a83afcde0fc53c71ae14d5a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3640512766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3067b45c167a3153a3a45711a7d022900ed5d21e17b7da3dcb86ce3b2a5cd9b`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Dec 2025 21:49:56 GMT
RUN Install update 10.0.26100.7462
# Thu, 08 Jan 2026 19:06:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 08 Jan 2026 19:06:59 GMT
ENV JULIA_VERSION=1.12.4
# Thu, 08 Jan 2026 19:07:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.4-win64.exe
# Thu, 08 Jan 2026 19:07:01 GMT
ENV JULIA_SHA256=6b0e030497bd1abc0c12054105e70f0c5600f312be1dadd728d9b6624f9f8940
# Thu, 08 Jan 2026 19:09:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 08 Jan 2026 19:09:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Mon, 08 Dec 2025 10:02:12 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890b21ccebaeedf053c6c32fb4fe8d98ab2c60496b12e6b730ac67df9096fc5b`  
		Last Modified: Tue, 09 Dec 2025 19:44:14 GMT  
		Size: 1.0 GB (1037813290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d126de1694a43d0102a4b151fadbf540a854e91ba7bd0acc8c78c53874728b7a`  
		Last Modified: Thu, 08 Jan 2026 19:25:01 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f66e44154192550e92a284d5674c77bcdea0477bc64f226edb46370cbffdb81`  
		Last Modified: Thu, 08 Jan 2026 19:25:01 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e819a62c3a1471c27d528140f81e81e17b7b299eb0d8049b399d06c84e7d16ea`  
		Last Modified: Thu, 08 Jan 2026 19:25:01 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3f9407a3698dd2472c340ea451a05c01d922a4f920bbb1d51928109beaaf78`  
		Last Modified: Thu, 08 Jan 2026 19:25:02 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75bde047c6a14ad49c470208b7ac4712cd4aa8bcd9c199a80adf07a51dcd6b5`  
		Last Modified: Thu, 08 Jan 2026 19:25:24 GMT  
		Size: 387.4 MB (387385755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:453ded3a3e51e437a30ef6b3707dcab798b1a26797612484da544e71c271533c`  
		Last Modified: Thu, 08 Jan 2026 19:25:02 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.20348.4529; amd64

```console
$ docker pull julia@sha256:93c9ee5b6de1057aded6e9f1de2c52ccddede5676ebaafb3fb0c2ff04bfd0eb2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2167349380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88388e5d18b5a3673edd7b202632b12ef2bcc69d67f0605dab480f37721ad97e`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Thu, 08 Jan 2026 20:57:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 08 Jan 2026 20:57:35 GMT
ENV JULIA_VERSION=1.12.4
# Thu, 08 Jan 2026 20:57:37 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.4-win64.exe
# Thu, 08 Jan 2026 20:57:39 GMT
ENV JULIA_SHA256=6b0e030497bd1abc0c12054105e70f0c5600f312be1dadd728d9b6624f9f8940
# Thu, 08 Jan 2026 21:03:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 08 Jan 2026 21:03:58 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60080bcdf91ac82d9335a1c9800f8aaa099ac4ac23b90a4054a48927c3a26993`  
		Last Modified: Thu, 08 Jan 2026 21:15:34 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c359ddfe0fd68cb005cd7e0bc4b03dbb728a55cec9d56cac3f95c7cbbd27be`  
		Last Modified: Thu, 08 Jan 2026 21:15:34 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b658395a5475e656d6091f6f0278cfdb8875b9c97f6d9c0df90a1587a99b61`  
		Last Modified: Thu, 08 Jan 2026 21:15:34 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e136e007a6f13a679296c716b7c77ba21942c30f1aaf4d904e479e82b9ace14`  
		Last Modified: Thu, 08 Jan 2026 21:15:34 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a6e003b6310cf9296a6e6035dcc2d11c0800e3286ca12418ba62442601e2831`  
		Last Modified: Thu, 08 Jan 2026 21:15:47 GMT  
		Size: 387.5 MB (387463550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e96149f0052c374567d3ddf528b36cc9e385b7545890288eedb58b4a7aa2229`  
		Last Modified: Thu, 08 Jan 2026 21:15:34 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
