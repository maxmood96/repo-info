## `julia:rc`

```console
$ docker pull julia@sha256:5a9444f298655a4df95043fc2a9f0fd615e63c963e2b6d5716ad18254958048d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `julia:rc` - linux; amd64

```console
$ docker pull julia@sha256:bf5428b77d04732cafdd7162e9ea5849b7ab8308428b9d5e8943fd27f3eab080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.7 MB (321704922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17dad230548d18f83ee69e013e9e9e23a343c648f00f6b47ccf41d2bb6d213ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Sun, 28 Sep 2025 11:59:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 28 Sep 2025 11:59:29 GMT
ENV JULIA_PATH=/usr/local/julia
# Sun, 28 Sep 2025 11:59:29 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 28 Sep 2025 11:59:29 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sun, 28 Sep 2025 11:59:29 GMT
ENV JULIA_VERSION=1.12.0-rc3
# Sun, 28 Sep 2025 11:59:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-rc3-linux-x86_64.tar.gz'; 			sha256='d89d6483c141160d893d71bd1ab87f6d56bc8d5762c35093c7644c3cbc1a9d1d'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-rc3-linux-aarch64.tar.gz'; 			sha256='1dfb20c6beaa1c4dbfbf6e8168b74e213023367990e35003d6b35d83579f0b11'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-rc3-linux-i686.tar.gz'; 			sha256='372fcd8135e0836394d8e0c5ab7ef4f768b91f3613c4f807a7bf71470893b7ac'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sun, 28 Sep 2025 11:59:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 28 Sep 2025 11:59:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 28 Sep 2025 11:59:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67f8a2af7a6aab2301f9ae5995ddc9168094446a13f34cee91ed3e6e21159ea`  
		Last Modified: Mon, 29 Sep 2025 17:55:25 GMT  
		Size: 6.2 MB (6242818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96053bdb028d62b978544b83647468e12650425173e2b347b33fed55dd6d46c5`  
		Last Modified: Mon, 29 Sep 2025 20:09:08 GMT  
		Size: 285.7 MB (285688237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d9e6faee3ccd4ac011854373604f5fb22eaad618b389d992d86666f7292513`  
		Last Modified: Mon, 29 Sep 2025 17:55:25 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:f0c046e57b6ce758e5eaac954b657fba75890c374eda488a1d9febfb13d434c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e19b252c1ed547f9c3cb6c1abc08e87d8e1ab6036f45f52475e1cd8e1334660`

```dockerfile
```

-	Layers:
	-	`sha256:3b9b702133f76093dcf8a4cd416b848f62ed03cceb4d10e52a69e26abc24c15b`  
		Last Modified: Mon, 29 Sep 2025 20:02:47 GMT  
		Size: 2.2 MB (2239479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1eecf972483478de7aed934e149bbc23624ac4a9233d571b4aa340c1ff0ef51`  
		Last Modified: Mon, 29 Sep 2025 20:02:48 GMT  
		Size: 17.2 KB (17219 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:f678d81437946a446eca6f25b5190a51ec0638eecd00e37d66516f2445f1ebfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.9 MB (341867179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5addff66f57b54ec34269762b04671be5b8832b6c6979cdfecc1c5c807379b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Sun, 28 Sep 2025 11:59:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 28 Sep 2025 11:59:29 GMT
ENV JULIA_PATH=/usr/local/julia
# Sun, 28 Sep 2025 11:59:29 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 28 Sep 2025 11:59:29 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sun, 28 Sep 2025 11:59:29 GMT
ENV JULIA_VERSION=1.12.0-rc3
# Sun, 28 Sep 2025 11:59:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-rc3-linux-x86_64.tar.gz'; 			sha256='d89d6483c141160d893d71bd1ab87f6d56bc8d5762c35093c7644c3cbc1a9d1d'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-rc3-linux-aarch64.tar.gz'; 			sha256='1dfb20c6beaa1c4dbfbf6e8168b74e213023367990e35003d6b35d83579f0b11'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-rc3-linux-i686.tar.gz'; 			sha256='372fcd8135e0836394d8e0c5ab7ef4f768b91f3613c4f807a7bf71470893b7ac'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sun, 28 Sep 2025 11:59:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 28 Sep 2025 11:59:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 28 Sep 2025 11:59:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf129ca8e8cc15d22d8a5cae7a1edebd6785a9dbb01f1454e287c51d32a8a79f`  
		Last Modified: Mon, 29 Sep 2025 17:59:06 GMT  
		Size: 6.2 MB (6153081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cce95111b7a9ab8d830c97a7aa46ac139cb42af38f22914ad1bfbc7aaad641c`  
		Last Modified: Mon, 29 Sep 2025 20:09:49 GMT  
		Size: 305.6 MB (305577094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4559b565a6a3d91e6df9d160076e7b2e6a8d0e0381a2b080fa1f78fd10450fbf`  
		Last Modified: Mon, 29 Sep 2025 17:59:06 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:010f998257c83ea426e5d392601206c4f3c845802acb26545d72716598101a12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f907f86d1508c4fbf5a0c57ae21cc8dba209f75e0ca293134c42488edf232e6`

```dockerfile
```

-	Layers:
	-	`sha256:2004eafaeb76b113f92669a6cfabbe9334aa155d627619e74c1f43911fc96f42`  
		Last Modified: Mon, 29 Sep 2025 20:02:52 GMT  
		Size: 2.2 MB (2239787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1516a34fca6f9005b49d1ab04de373a526e0a661f4aa32ea237fb757726b014`  
		Last Modified: Mon, 29 Sep 2025 20:02:53 GMT  
		Size: 17.4 KB (17362 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - linux; 386

```console
$ docker pull julia@sha256:5505131c7352a565c277f8ede55b018ffde60d44d8708eedb52d4d6a4df2158f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.5 MB (267480874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ea07707a5ba5243ceb022f9b649cd51d73190d38a594f81f32d1b30f9d97d7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
# Sun, 28 Sep 2025 11:59:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 28 Sep 2025 11:59:29 GMT
ENV JULIA_PATH=/usr/local/julia
# Sun, 28 Sep 2025 11:59:29 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 28 Sep 2025 11:59:29 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sun, 28 Sep 2025 11:59:29 GMT
ENV JULIA_VERSION=1.12.0-rc3
# Sun, 28 Sep 2025 11:59:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-rc3-linux-x86_64.tar.gz'; 			sha256='d89d6483c141160d893d71bd1ab87f6d56bc8d5762c35093c7644c3cbc1a9d1d'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-rc3-linux-aarch64.tar.gz'; 			sha256='1dfb20c6beaa1c4dbfbf6e8168b74e213023367990e35003d6b35d83579f0b11'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-rc3-linux-i686.tar.gz'; 			sha256='372fcd8135e0836394d8e0c5ab7ef4f768b91f3613c4f807a7bf71470893b7ac'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sun, 28 Sep 2025 11:59:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 28 Sep 2025 11:59:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 28 Sep 2025 11:59:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:d6e01c57fc6d674eef68e6bfe57a080b0a70c1c25810b7d6e769151bad3645bf`  
		Last Modified: Mon, 08 Sep 2025 21:12:32 GMT  
		Size: 31.3 MB (31289784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3e61cbf4dd256f423a4015b544e0ce3c8b3b6c9d82a1ef17ebd62e62d21f85`  
		Last Modified: Mon, 29 Sep 2025 17:51:25 GMT  
		Size: 6.4 MB (6427763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ecf878d85496241b4c755f9524bdbb63039ba9c7fdfdd0513ccec181de6846`  
		Last Modified: Mon, 29 Sep 2025 20:09:06 GMT  
		Size: 229.8 MB (229762954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2485f385b83cc499858c333f58fac0289f25f91d9a0b778df82890a4fdf5fe`  
		Last Modified: Mon, 29 Sep 2025 17:51:24 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:3549150a0e02e0a5b321ed7ab09eaeac279f3db3d8cc3f68eaa0e39dbdf4ff44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2253789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8911e43bd3c2fc065633776999e3e0fd1c36eecc2ddf219aff1fd1e851db3ab2`

```dockerfile
```

-	Layers:
	-	`sha256:abfc31f46b1447a3ca8386976889a8dd874e9767560ba96929b7bab8258ee31c`  
		Last Modified: Mon, 29 Sep 2025 20:02:56 GMT  
		Size: 2.2 MB (2236614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b9e17e5755460d6e8fe4f3a225751695db13aef35cadf0ca1bb1c7333b5187f`  
		Last Modified: Mon, 29 Sep 2025 20:02:57 GMT  
		Size: 17.2 KB (17175 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - windows version 10.0.26100.6584; amd64

```console
$ docker pull julia@sha256:561937bf6e37457b2aa4707c3ff040b3dea59225f94d30532553fcf692f8f7c8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 GB (3869007100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:037ba1986027ea1cb6bec88fe9db7627cc36e62ee7af73e9947a5dbb92d20f67`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Mon, 29 Sep 2025 17:52:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 29 Sep 2025 17:52:22 GMT
ENV JULIA_VERSION=1.12.0-rc3
# Mon, 29 Sep 2025 17:52:23 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-rc3-win64.exe
# Mon, 29 Sep 2025 17:52:24 GMT
ENV JULIA_SHA256=4700e3325fe8d8c8f209fe09aa95928ff1c65b45fdf2968124bb143c5c59aded
# Mon, 29 Sep 2025 17:54:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Mon, 29 Sep 2025 17:54:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dc1e52f9bc29ce53d26b523c04988f69995788c22f43dc5eef117a6b5b69ed2`  
		Last Modified: Mon, 29 Sep 2025 18:11:27 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d667d6ca0ce99f83e02ab6dfd13017d89a62db952a3adbfacd25b741d40cbffe`  
		Last Modified: Mon, 29 Sep 2025 18:11:27 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f97168be5efa1c6f5fe3c5d033f6b92569eec1324b72371efdfb4cdd9c5688e`  
		Last Modified: Mon, 29 Sep 2025 18:11:27 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1313b88e9837ba5ee3a39b8cdf814429858a1118b5ef34cd7311d90b9ea2e5`  
		Last Modified: Mon, 29 Sep 2025 18:11:27 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2c7cc3abd0694dc02e2d589325c8e7607e467a44e89089519146fe297448d5f`  
		Last Modified: Mon, 29 Sep 2025 20:03:25 GMT  
		Size: 297.6 MB (297560786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5a7a1f6a11c973fa364d5ab8e67ee983e78caeec93e2994dded506010409a4`  
		Last Modified: Mon, 29 Sep 2025 18:11:27 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc` - windows version 10.0.20348.4171; amd64

```console
$ docker pull julia@sha256:6b158b2ae86f1a22218959e920b5e0c3da0086252c7465f0f99a8eaf3748c42d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2579659431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14e728f95378332db793877542399afa53751f58ae05ec4d1606acad128a90a9`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Mon, 29 Sep 2025 18:14:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 29 Sep 2025 18:14:13 GMT
ENV JULIA_VERSION=1.12.0-rc3
# Mon, 29 Sep 2025 18:14:14 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-rc3-win64.exe
# Mon, 29 Sep 2025 18:14:16 GMT
ENV JULIA_SHA256=4700e3325fe8d8c8f209fe09aa95928ff1c65b45fdf2968124bb143c5c59aded
# Mon, 29 Sep 2025 18:18:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Mon, 29 Sep 2025 18:18:38 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3662dfe36956d8cc7d770032f6242679aa97aa455b257e51284077f5c991083`  
		Last Modified: Mon, 29 Sep 2025 18:29:15 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ec2a6551600fc1aa44df9306e276fa86ab75e73277994e82d219f3ef0149ee`  
		Last Modified: Mon, 29 Sep 2025 18:29:15 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66436db09c21c6c1eb91810bd524cac80b897e605d8577712c23980ab21b317c`  
		Last Modified: Mon, 29 Sep 2025 18:29:15 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969246bc70379a38f812334714440f7bcfbbf827957a92dc2c4544f2d7211783`  
		Last Modified: Mon, 29 Sep 2025 18:29:15 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a23a30b61012f7a59fb4d441266b7a8178c9bca3ea1af1265c37937cba86e0`  
		Last Modified: Mon, 29 Sep 2025 20:03:26 GMT  
		Size: 297.5 MB (297507925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7fd026e3d12b4a1dfe27d3afbcb7966f972c49e4ddf6bb34827fea1990529c3`  
		Last Modified: Mon, 29 Sep 2025 18:29:15 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
