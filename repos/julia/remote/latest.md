## `julia:latest`

```console
$ docker pull julia@sha256:6ac25836e50e0bd97bf108a9f8788ad88ee3db807cdc54d73426bb7572fb32b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `julia:latest` - linux; amd64

```console
$ docker pull julia@sha256:dda96615191c8ffb51688525bf9c6d0b781deaf5e940d4d6bfb40be56ea1f16d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.0 MB (326001748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09128b62bab05bd56218e3d617610af127915c5f5475bd5ce18ccb0c4361b31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Sat, 06 Dec 2025 01:08:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Dec 2025 01:08:27 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 06 Dec 2025 01:08:27 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Dec 2025 01:08:27 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 06 Dec 2025 01:08:27 GMT
ENV JULIA_VERSION=1.12.2
# Sat, 06 Dec 2025 01:08:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.2-linux-x86_64.tar.gz'; 			sha256='a6d0c39ea57303ebcffa7a8d453429b86eb271e150c7cb0f5958fe65909b493a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.2-linux-i686.tar.gz'; 			sha256='e7492e2454ecfd03f4da6fd30fb60391d184128bf683c96d1ea6f13cd35a20c8'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.2-linux-aarch64.tar.gz'; 			sha256='0383a2ce378b64356269f6f15e612f344523f507a9753f71a0b64ca02092445b'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sat, 06 Dec 2025 01:08:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 06 Dec 2025 01:08:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Dec 2025 01:08:27 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c622a722f005d263b1954f3aa819ef31ebb434e5b191255e7187784e6ff69601`  
		Last Modified: Sat, 06 Dec 2025 01:09:27 GMT  
		Size: 6.2 MB (6242894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb7af1323ddf6c4dfd701244fc3cd5fb18daa09465934ea4fcf4baea406bf72`  
		Last Modified: Sat, 06 Dec 2025 01:10:27 GMT  
		Size: 290.0 MB (289981997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4f685b21e5624f1812aa0d5541b91b9c959196b94f8e15c8802feaee555fa5`  
		Last Modified: Sat, 06 Dec 2025 01:09:26 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:2749c05d737f12ff48c3cc56001ba0f163bcb80b825b6d875a8f0caf4139899b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df82674101d98825cca4e3ee1ee1dd3ba6cbe67cf6020139a77d9911e054c87e`

```dockerfile
```

-	Layers:
	-	`sha256:ea92afb6b85f126cd42432bbfb43f260f5649ece9850683d45328282cadd548d`  
		Last Modified: Sat, 06 Dec 2025 03:02:29 GMT  
		Size: 2.2 MB (2240123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccaacda2e03d5a2e5ffa92614d3bf144efa919c379b5304aa46f31fafe127934`  
		Last Modified: Sat, 06 Dec 2025 03:02:30 GMT  
		Size: 17.7 KB (17689 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:3fb3b282a105f4c690e867351a305ac10fbf8ea2e51edb03a84dba982c1b9104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.3 MB (347276187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a898ef47c838a9465643f6cfe462dc6ab967bf43f2c6519fd20754df5b9b34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Sat, 06 Dec 2025 01:07:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Dec 2025 01:07:38 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 06 Dec 2025 01:07:38 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Dec 2025 01:07:38 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 06 Dec 2025 01:07:38 GMT
ENV JULIA_VERSION=1.12.2
# Sat, 06 Dec 2025 01:07:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.2-linux-x86_64.tar.gz'; 			sha256='a6d0c39ea57303ebcffa7a8d453429b86eb271e150c7cb0f5958fe65909b493a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.2-linux-i686.tar.gz'; 			sha256='e7492e2454ecfd03f4da6fd30fb60391d184128bf683c96d1ea6f13cd35a20c8'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.2-linux-aarch64.tar.gz'; 			sha256='0383a2ce378b64356269f6f15e612f344523f507a9753f71a0b64ca02092445b'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sat, 06 Dec 2025 01:07:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 06 Dec 2025 01:07:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Dec 2025 01:07:38 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b567f66ed007f6551fe2d88e3f3a174dcfa636b56db683bf915eb31c77c6d699`  
		Last Modified: Sat, 06 Dec 2025 01:08:42 GMT  
		Size: 6.2 MB (6153421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a6a844e9011306ee6ab1784d0eeb6b59b555288afada023bd7c957b8743206`  
		Last Modified: Sat, 06 Dec 2025 01:10:29 GMT  
		Size: 311.0 MB (310983785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e8865ba5e47efa6215b13ca514557f873db355ab6b67fcc007a3755f394e80`  
		Last Modified: Sat, 06 Dec 2025 01:08:41 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:66a1310f84633c096214f3aaab8a0a605760aa32bdec80ec7fb48a4334dd1828
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38c9a4b4ec786715a33de4bad85015151db443e0a4928e5b795caf9dbeeeeb44`

```dockerfile
```

-	Layers:
	-	`sha256:0f165b87ccab48332681490cdd60765d067fce92918aa21e4022249b4a9cb752`  
		Last Modified: Sat, 06 Dec 2025 03:02:33 GMT  
		Size: 2.2 MB (2240455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2255833f9d30a810488bc772a00e710f5330b9741832b94ea5c2d89d4850880c`  
		Last Modified: Sat, 06 Dec 2025 03:02:34 GMT  
		Size: 17.9 KB (17856 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; 386

```console
$ docker pull julia@sha256:ad97e82c07b4d8853fd12a23c776d86b9f459ee5f34347b25e53c11e0ec2b628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268889785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d31b057b75cf7523d9479db66be1ffd3b70932826a8d8d531c20bd5203234fd3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Sat, 06 Dec 2025 01:07:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Dec 2025 01:07:48 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 06 Dec 2025 01:07:48 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Dec 2025 01:07:48 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 06 Dec 2025 01:07:48 GMT
ENV JULIA_VERSION=1.12.2
# Sat, 06 Dec 2025 01:07:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.2-linux-x86_64.tar.gz'; 			sha256='a6d0c39ea57303ebcffa7a8d453429b86eb271e150c7cb0f5958fe65909b493a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.2-linux-i686.tar.gz'; 			sha256='e7492e2454ecfd03f4da6fd30fb60391d184128bf683c96d1ea6f13cd35a20c8'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.2-linux-aarch64.tar.gz'; 			sha256='0383a2ce378b64356269f6f15e612f344523f507a9753f71a0b64ca02092445b'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sat, 06 Dec 2025 01:07:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 06 Dec 2025 01:07:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Dec 2025 01:07:48 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7ab280841eb2d24ca23c5205ed4c99f2348475a55382d2fb8135a091d48912`  
		Last Modified: Sat, 06 Dec 2025 01:08:34 GMT  
		Size: 6.4 MB (6427615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff01a93f31d731428d6946ee8a4c510056b6825e2bad8690b45d60fb2205c2b3`  
		Last Modified: Sat, 06 Dec 2025 01:08:43 GMT  
		Size: 231.2 MB (231168729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd7d3c8b4ff02da5bd1ae966b323fd23a615bc754edf3e4e6bc4ea8782f2448`  
		Last Modified: Sat, 06 Dec 2025 01:08:33 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:66532e40cee0685281ed7ed7d968d990f9fb7adcc5946bde7bbe1ff4cda3833b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:928cc800c6a8cade3b18d874b792a38392dbc50d793654751cc312ca91f3d186`

```dockerfile
```

-	Layers:
	-	`sha256:7b08143b9be3b5622f57294bef344473e446e73056f32e393cbe9bb374b360bd`  
		Last Modified: Sat, 06 Dec 2025 03:02:37 GMT  
		Size: 2.2 MB (2237248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c94db98b38bb3c1d121fae5b6a80b001bbef84532ab09e01d1c3df6c88164c8b`  
		Last Modified: Sat, 06 Dec 2025 03:02:38 GMT  
		Size: 17.6 KB (17634 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:04f3a5adc3f75a66cf062823539f9b514a191acf479142c0785838f9c8a9914c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3621475366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe0f809a4decf0e532fbb1c9fed3e291db5a0cf3141761801dacfef881ceda7`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Sat, 06 Dec 2025 00:40:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 06 Dec 2025 01:06:24 GMT
ENV JULIA_VERSION=1.12.2
# Sat, 06 Dec 2025 01:06:24 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.2-win64.exe
# Sat, 06 Dec 2025 01:06:25 GMT
ENV JULIA_SHA256=b8c6ffd3f760e088820f0f208b799167a02d528df467337852ffcc599eaa8e7e
# Sat, 06 Dec 2025 01:08:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Sat, 06 Dec 2025 01:08:06 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Mon, 08 Dec 2025 10:02:12 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d491b064d08a64d94dcb03d80d556f4a1ba7a494f3762485661160f954d6ca`  
		Last Modified: Sat, 06 Dec 2025 01:00:17 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429d7e15e5fb8ff3aafac014029247247fc27b0420c9d783c322ae028a1661a7`  
		Last Modified: Sat, 06 Dec 2025 01:09:29 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7058b522592d35ca406ae0fbb68ded735b1f973bf3c1dd2758aec0b53accb028`  
		Last Modified: Sat, 06 Dec 2025 01:09:29 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d96febdaf0b87da4d2ab9284c507758fa63828aa37783b8fcce43af7ba37bde`  
		Last Modified: Sat, 06 Dec 2025 01:09:30 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a588353a6df13364f0fdb03407b0a19747f441dbcb1996b841caf339b11ed2f7`  
		Last Modified: Sat, 06 Dec 2025 01:09:35 GMT  
		Size: 386.0 MB (386013023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c62e1bdf1d24a83b06fcf91e5a6be3d59a80e5796f81afcf035f98af9b2dd951`  
		Last Modified: Sat, 06 Dec 2025 01:09:30 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:182b17c903a2a430ca241abf41714877477e4a48098d97015efd5dacc9146a29
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2156064808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40a0a6fa09d0c43d7168f5e629beb272ed9aa78e88a1a938239bf46c19de25d2`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Sat, 06 Dec 2025 00:35:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 06 Dec 2025 01:06:24 GMT
ENV JULIA_VERSION=1.12.2
# Sat, 06 Dec 2025 01:06:25 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.2-win64.exe
# Sat, 06 Dec 2025 01:06:25 GMT
ENV JULIA_SHA256=b8c6ffd3f760e088820f0f208b799167a02d528df467337852ffcc599eaa8e7e
# Sat, 06 Dec 2025 01:09:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Sat, 06 Dec 2025 01:09:35 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8462076761531ece541cabbff8aa81904d45ff8a160c631ad6c756c28992e1c1`  
		Last Modified: Sat, 06 Dec 2025 00:45:14 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ccf31c85b482c150ed97cfc6f6b268ddf0091d66cb56eb993d8641f2cefb61`  
		Last Modified: Sat, 06 Dec 2025 01:10:49 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596f1f181f88ec0f43cdacbea9ab02299e6c80e2369605e91137b1f1b51982a4`  
		Last Modified: Sat, 06 Dec 2025 01:10:46 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a89e783b8f4296a56d315dfe1eb7b5d26a9e81f2a928f5f335893ce6078bd078`  
		Last Modified: Sat, 06 Dec 2025 01:10:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c6ebd1f1169d4079f949a72507f16c941c87eee6bfc01831ec3f1cd6d6c301`  
		Last Modified: Sat, 06 Dec 2025 01:12:43 GMT  
		Size: 386.1 MB (386096781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd62c859283ed30563bad9938bcf852fcc50b5f4f140b75eb217f60bcd4719d`  
		Last Modified: Sat, 06 Dec 2025 01:10:47 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
