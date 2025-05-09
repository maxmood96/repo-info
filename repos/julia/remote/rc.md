## `julia:rc`

```console
$ docker pull julia@sha256:9ed8e8277fb097e4c50e402fcec18d12c91c6b45080cc89023cd2215e9095daa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 9
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.26100.3781; amd64
	-	windows version 10.0.20348.3566; amd64
	-	windows version 10.0.17763.7249; amd64

### `julia:rc` - linux; amd64

```console
$ docker pull julia@sha256:6635fa80151b95b78c302946c05a7ef05c86edd44c5c11291f4efe5730511cd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.1 MB (328128423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b768d8d055db5919d75550217cd245fd515120e8536f05d9824e3ea2770842e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 25 Apr 2025 23:13:55 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Fri, 25 Apr 2025 23:13:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 25 Apr 2025 23:13:55 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 25 Apr 2025 23:13:55 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Apr 2025 23:13:55 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 25 Apr 2025 23:13:55 GMT
ENV JULIA_VERSION=1.12.0-beta2
# Fri, 25 Apr 2025 23:13:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-beta2-linux-x86_64.tar.gz'; 			sha256='b7466702ec9ceaaf0565acac7df7c26316a9af3dbb048d01797e71e4dbaaa924'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-beta2-linux-aarch64.tar.gz'; 			sha256='46c3f128f12fef5b22133b540a9fedbbefb412b23f7b49f1cf278174a2959dd3'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-beta2-linux-i686.tar.gz'; 			sha256='fddddc7bce50adae38b45fbeb9b05ea2c8062cc20d6dd50d5879c0818cf01c0b'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Fri, 25 Apr 2025 23:13:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 23:13:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 23:13:55 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Thu, 08 May 2025 17:04:38 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caadbadaee131b82f1bf719c1ffb422491c374a8227dd6e7d2c47a1cf95f9b7c`  
		Last Modified: Thu, 08 May 2025 18:28:37 GMT  
		Size: 5.7 MB (5713427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97df4b65b34c03e38aad963545dd11029e5791a98286b8e5ac45e5fd9ca9d066`  
		Last Modified: Thu, 08 May 2025 18:28:46 GMT  
		Size: 294.2 MB (294186987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d22f170d531c62af8b2ba66552e5fb8f5e9121abcacf985a383cae414d76da5`  
		Last Modified: Thu, 08 May 2025 18:28:38 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:5f5e3af0dd7dc1ac6df718f55d4929dacb1e398110857888ecf7546916801cec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b71c15074ae2c706c848e80ee7e320c1a589fdd69947213cd565c9b1c2b7e583`

```dockerfile
```

-	Layers:
	-	`sha256:afab9542f121c7f2ede6ec361dba12fbe473f2d29812c82e17efcf8277bb2bfd`  
		Last Modified: Mon, 28 Apr 2025 21:43:19 GMT  
		Size: 2.4 MB (2446248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d1fdf6a05f5d34eb3f8c446b6956faf026e080a652ff261be3085b31f644ef1`  
		Last Modified: Mon, 28 Apr 2025 21:43:19 GMT  
		Size: 17.3 KB (17271 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:19986fadb65ca87b5b03dec6f8eb85108ab438576fbbf9362b102fb3108dcaf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.8 MB (348813183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c8f468882f005d10bbe4c44b7e7fbd47a80267aa4fd72fb677d47cd0cf9064c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 25 Apr 2025 23:13:55 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Fri, 25 Apr 2025 23:13:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 25 Apr 2025 23:13:55 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 25 Apr 2025 23:13:55 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Apr 2025 23:13:55 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 25 Apr 2025 23:13:55 GMT
ENV JULIA_VERSION=1.12.0-beta2
# Fri, 25 Apr 2025 23:13:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-beta2-linux-x86_64.tar.gz'; 			sha256='b7466702ec9ceaaf0565acac7df7c26316a9af3dbb048d01797e71e4dbaaa924'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-beta2-linux-aarch64.tar.gz'; 			sha256='46c3f128f12fef5b22133b540a9fedbbefb412b23f7b49f1cf278174a2959dd3'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-beta2-linux-i686.tar.gz'; 			sha256='fddddc7bce50adae38b45fbeb9b05ea2c8062cc20d6dd50d5879c0818cf01c0b'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Fri, 25 Apr 2025 23:13:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 23:13:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 23:13:55 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c23a06ea64187f3b06926c8e0226c9000d3c038da0bf7de39452382de736dc`  
		Last Modified: Thu, 08 May 2025 17:29:01 GMT  
		Size: 5.5 MB (5538350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1622528dd17613920a23a4ddfc21eccc2db43dfc63f670a793c5db357fa3d3d1`  
		Last Modified: Mon, 28 Apr 2025 22:27:50 GMT  
		Size: 315.2 MB (315207842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3001ba970a959ae7e967248f2a17675fd51dbd328782a04fe5565b7545da2c6c`  
		Last Modified: Mon, 28 Apr 2025 22:27:43 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:78e08ab2563c75551cef3602c723d852c60f32d557d9cecf3834b39f730f59dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65404fd89fc28fa488a2078002e8520a57dd264c18e8690507fa88b2c25bc68b`

```dockerfile
```

-	Layers:
	-	`sha256:874f2335a3450ebf48adc5846eb2b332fc461a10ac618267cc4b99ba38f6b364`  
		Last Modified: Mon, 28 Apr 2025 22:27:43 GMT  
		Size: 2.4 MB (2446547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ed5facd0a49ae372298a2e007a45fb75342671a285ef70a93856c94e7e6c868`  
		Last Modified: Mon, 28 Apr 2025 22:27:43 GMT  
		Size: 17.4 KB (17414 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - linux; 386

```console
$ docker pull julia@sha256:c961373a1b762b94e1daf6648fd603321bbc25ff0a55f7f6463e3c26534296ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.1 MB (271108804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b839da6947ca66316f07eed96c990db32e7d1c74bb050843d4920a83afc4725d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 25 Apr 2025 23:13:55 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
# Fri, 25 Apr 2025 23:13:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 25 Apr 2025 23:13:55 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 25 Apr 2025 23:13:55 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Apr 2025 23:13:55 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 25 Apr 2025 23:13:55 GMT
ENV JULIA_VERSION=1.12.0-beta2
# Fri, 25 Apr 2025 23:13:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-beta2-linux-x86_64.tar.gz'; 			sha256='b7466702ec9ceaaf0565acac7df7c26316a9af3dbb048d01797e71e4dbaaa924'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-beta2-linux-aarch64.tar.gz'; 			sha256='46c3f128f12fef5b22133b540a9fedbbefb412b23f7b49f1cf278174a2959dd3'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-beta2-linux-i686.tar.gz'; 			sha256='fddddc7bce50adae38b45fbeb9b05ea2c8062cc20d6dd50d5879c0818cf01c0b'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Fri, 25 Apr 2025 23:13:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 23:13:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 23:13:55 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ad2e653a01d32a9a8676730797453c924f9d10fe1414178e7a26c35132c3691e`  
		Last Modified: Thu, 08 May 2025 17:08:57 GMT  
		Size: 29.2 MB (29210866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca3499bc7793646db90fb3333faf5639f2a00fc06c01dfac6bf23ca6b5a45f1`  
		Last Modified: Mon, 28 Apr 2025 21:43:09 GMT  
		Size: 5.9 MB (5872255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e276528553f50615fef747e91f59e755b481db7ab5f153c7af4c66bf3a8c661`  
		Last Modified: Mon, 28 Apr 2025 21:43:15 GMT  
		Size: 236.0 MB (236025315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0c2c67a0e15df75c5b14915ec28cbf70084cd33d5f83f760699b94728062e0`  
		Last Modified: Mon, 28 Apr 2025 21:43:08 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:1d6ccfebffe17b68989e2dfa6a609d50b781450abbfbf6f9040d77f8bd46307b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e668880c307e1183757dd38800e901801bdac5ded805b29468c88b4932fd43e`

```dockerfile
```

-	Layers:
	-	`sha256:36747ca45591818539f73f697f7cef68998f1f769ad83653e5febe51ba706422`  
		Last Modified: Mon, 28 Apr 2025 21:43:09 GMT  
		Size: 2.4 MB (2443331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1284d0254c095d4442a45854ce868a32fc965699e713940fa6983c0211e462cf`  
		Last Modified: Mon, 28 Apr 2025 21:43:08 GMT  
		Size: 17.2 KB (17227 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - windows version 10.0.26100.3781; amd64

```console
$ docker pull julia@sha256:78955389ef1cdf07a3a149410fee0a6058b0c0f5d82da8a76202a5e68fc01fca
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3684252253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18b47fe53a1a1d22f0a0ce2efbdbe44baf2cdbd6a759d77f7273260eb31a15ac`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Tue, 15 Apr 2025 10:03:37 GMT
RUN Install update 10.0.26100.3781
# Mon, 28 Apr 2025 18:14:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 28 Apr 2025 18:14:10 GMT
ENV JULIA_VERSION=1.12.0-beta2
# Mon, 28 Apr 2025 18:14:11 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-beta2-win64.exe
# Mon, 28 Apr 2025 18:14:12 GMT
ENV JULIA_SHA256=92421914379d45e328f4d7e531c26cc7c4504675b25f5d79872f41fdd98e5bed
# Mon, 28 Apr 2025 18:15:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Mon, 28 Apr 2025 18:15:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a55b9bd12cfb5d81d64963683e6d5d0ba9423233c85140eff135128a64f7ee`  
		Last Modified: Thu, 08 May 2025 17:36:06 GMT  
		Size: 1.2 GB (1179854238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:609dea27acd35e678323144831aa695da908bacdca53a275a1ba2688f48f44a4`  
		Last Modified: Mon, 28 Apr 2025 18:15:34 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491f7b9b66336b21f4c5e263347a229bbcddb5e12fb15b9c528d0125940d394a`  
		Last Modified: Mon, 28 Apr 2025 18:15:32 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36010aa1b6eb5c5d447360ec6a4b3ba4b466978e8506180bd5ad12953884a3a3`  
		Last Modified: Mon, 28 Apr 2025 18:15:32 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cbeb2b5dc9c5d449b80f00b8e4f8f5e8634712e698c1cc397c7148bb8db8019`  
		Last Modified: Mon, 28 Apr 2025 18:15:33 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e87e03320ab91f85853ffdc60e271d6261e6a1b5afcead5948035aead72a3c3`  
		Last Modified: Mon, 28 Apr 2025 18:16:18 GMT  
		Size: 289.1 MB (289084296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54a3fae4768f31cbf53e946aa9a12efc58626c5028cc5019a025c1c99af186c6`  
		Last Modified: Mon, 28 Apr 2025 18:15:32 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc` - windows version 10.0.20348.3566; amd64

```console
$ docker pull julia@sha256:82c36562c442e36420de0dc974fd05239fa341dd8426c8ddf6edeae9b4e85c03
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2562559751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b89918adfb7759b89997ad67410ed2aefcc51cd449e86228ee8cf51d64fe7a3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Mon, 28 Apr 2025 18:17:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 28 Apr 2025 18:17:59 GMT
ENV JULIA_VERSION=1.12.0-beta2
# Mon, 28 Apr 2025 18:18:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-beta2-win64.exe
# Mon, 28 Apr 2025 18:18:01 GMT
ENV JULIA_SHA256=92421914379d45e328f4d7e531c26cc7c4504675b25f5d79872f41fdd98e5bed
# Mon, 28 Apr 2025 18:19:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Mon, 28 Apr 2025 18:19:20 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6ee194dfee460cc53e0f761b7ff976c08380d6cd1e70cc50ff92cfa99d176`  
		Last Modified: Thu, 08 May 2025 17:22:47 GMT  
		Size: 811.4 MB (811390127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa0d58749a4597742bccf0680c763b881141dd181f413f5f33223feb36cb276`  
		Last Modified: Fri, 09 May 2025 08:00:49 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1049c39d0d9c306ffbc1461cbe2e4a66f34efea3880015eedd337ad230d0b959`  
		Last Modified: Fri, 09 May 2025 08:00:50 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a88e2404dd1736b9677139ac22b631faaf927d0768eee2dcabbf1b28d0e8a5`  
		Last Modified: Fri, 09 May 2025 08:00:49 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c2ce9c78fc4dacb3ffe2e3b5320e0721f6e83ccdcc8ddb444c98a650abd71a3`  
		Last Modified: Fri, 09 May 2025 08:00:49 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00687c330756524eae32cf76bd81cf3a1b919a0728fd82c1c7f7330354e60121`  
		Last Modified: Mon, 28 Apr 2025 18:20:01 GMT  
		Size: 289.0 MB (288970784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16f1e7c4d264658568bdcd18524e9d6892b1a4fd96e462150ff5d7ac4cd9ec6`  
		Last Modified: Fri, 09 May 2025 08:00:50 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc` - windows version 10.0.17763.7249; amd64

```console
$ docker pull julia@sha256:90887a42840477af7b42ae1941c700ea81847e9ea413e7556a3fc06c7a633d92
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2454506616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80bb0a9c700b8b6b827f024cb9ede930537021503749da187479aba71ba801a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Mon, 28 Apr 2025 18:16:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 28 Apr 2025 18:16:11 GMT
ENV JULIA_VERSION=1.12.0-beta2
# Mon, 28 Apr 2025 18:16:14 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-beta2-win64.exe
# Mon, 28 Apr 2025 18:16:18 GMT
ENV JULIA_SHA256=92421914379d45e328f4d7e531c26cc7c4504675b25f5d79872f41fdd98e5bed
# Mon, 28 Apr 2025 18:18:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Mon, 28 Apr 2025 18:18:49 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Thu, 08 May 2025 17:14:51 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139daca1231c3dc6c386d14ef757302c18a7287c04e6d802c87e44c947149134`  
		Last Modified: Fri, 09 May 2025 12:08:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1bf971f69786e98e28e5c243d4b549bd6fcacf21db2c4f0516e7b25e65c927`  
		Last Modified: Fri, 09 May 2025 12:08:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e7a8ad1b9c05731b73aa382c432bf22158c92e669c9ba4ec03dcfdfb76261a`  
		Last Modified: Fri, 09 May 2025 12:08:49 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b7c0ced206a15942175711ed4fe1dcd17b1ecca73beec002b4bcb8109cd75a`  
		Last Modified: Fri, 09 May 2025 12:08:48 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:633a017d89b1a58b46f2549215fcfbcfc7318cd39d00a983a4771a5e5e7fc08e`  
		Last Modified: Mon, 28 Apr 2025 18:19:32 GMT  
		Size: 289.0 MB (288974358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:534319338f74f12d33ae69a6a8987cf98bdfcaab457d1502f74f32e3975f46a8`  
		Last Modified: Fri, 09 May 2025 12:08:48 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
