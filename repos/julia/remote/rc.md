## `julia:rc`

```console
$ docker pull julia@sha256:be44ecd1f090afdae61fc93d5eae21166b6a712cfa64c4c46bfe0031f7f62111
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `julia:rc` - linux; amd64

```console
$ docker pull julia@sha256:5947cca876a6ad7539ad68d0c47ff05acc07bbfb8e5663b0553306e8badd4112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.4 MB (345431596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2895025573ac08f6eebd3e47d397e51bc335fba0a631ccb4511811f7e98f813f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:22:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:22:27 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 08 May 2026 19:22:27 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:22:27 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 08 May 2026 19:22:27 GMT
ENV JULIA_VERSION=1.13.0-rc1
# Fri, 08 May 2026 19:22:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-rc1-linux-x86_64.tar.gz'; 			sha256='94c501d83aa46fad188894a31db093c6d065bbab94346645c775876066ec1b78'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-rc1-linux-i686.tar.gz'; 			sha256='1e758cfe0ba45a9b5313ff732ff5aa0d4f1927129e1b207e5e6c51e35ed9abb4'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-rc1-linux-aarch64.tar.gz'; 			sha256='0e08d6410e76a51b6825aed34c9e20fd5778b35cc4b406dd8eb8bd402d8df705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Fri, 08 May 2026 19:22:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:22:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:22:27 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab77579b1922e22fca45b02d562a739a8fdc1f31e4302b9cbb605cb275292389`  
		Last Modified: Fri, 08 May 2026 19:23:12 GMT  
		Size: 6.2 MB (6247090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ad43f27e105c83a91b1af0035f72aa34b5ed58ec1722c036417e11787930ac`  
		Last Modified: Fri, 08 May 2026 19:23:18 GMT  
		Size: 309.4 MB (309403909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93cf8fb8ed1de9c8434a1d064fbc6b814054ed8b8dd26b8d9b3700a9f36328c6`  
		Last Modified: Fri, 08 May 2026 19:23:12 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:35debd6a3318a3a908942135753064690a2490c24f2f2b20335699847535b1a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22122dfb87a07a4ab2abf246fcf3971067c63fe412f889d1e10c017cd579023b`

```dockerfile
```

-	Layers:
	-	`sha256:50715123b86412245456a12918f8867d42d8b393948fd2df9778e9ee1b246fcb`  
		Last Modified: Fri, 08 May 2026 19:23:12 GMT  
		Size: 2.2 MB (2240907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca394b489c306211c4e555e5e6a71fe184a7781f2bb939b9ec905e303635a009`  
		Last Modified: Fri, 08 May 2026 19:23:12 GMT  
		Size: 17.2 KB (17161 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:64b0d075380aea85d630da69734082bb7216e96628c713d99391a57f3938ea0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.1 MB (370107055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:838f69cf5aa9e0dae66034ba637d3b1bc3b846a2eb0fbe528615928a0f06d581`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:20:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:21:29 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 08 May 2026 19:21:29 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:21:29 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 08 May 2026 19:21:29 GMT
ENV JULIA_VERSION=1.13.0-rc1
# Fri, 08 May 2026 19:21:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-rc1-linux-x86_64.tar.gz'; 			sha256='94c501d83aa46fad188894a31db093c6d065bbab94346645c775876066ec1b78'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-rc1-linux-i686.tar.gz'; 			sha256='1e758cfe0ba45a9b5313ff732ff5aa0d4f1927129e1b207e5e6c51e35ed9abb4'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-rc1-linux-aarch64.tar.gz'; 			sha256='0e08d6410e76a51b6825aed34c9e20fd5778b35cc4b406dd8eb8bd402d8df705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Fri, 08 May 2026 19:21:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:21:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:21:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c326e4356863911ec57dcad175191cecc464fee161c1255190be6e61690a9f`  
		Last Modified: Fri, 08 May 2026 19:20:50 GMT  
		Size: 6.2 MB (6154403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb2af28196db51d060c5f7e074e3ef8dd1f046cc129430e9c93077bf3b4c569`  
		Last Modified: Fri, 08 May 2026 19:22:29 GMT  
		Size: 333.8 MB (333808642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fc84cff2f3e376b79c9b80129cb15c4a6ff5d9d58d201852895f1a0ffa15d9`  
		Last Modified: Fri, 08 May 2026 19:22:16 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:2077e00cb826c86d2d2f41f8333fb4739983d102ad969358e1f5852f9f0b469a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a6a781e67ed9ebd6009b5c56f5905279491ce61bcca11fc263b538f3b093d2f`

```dockerfile
```

-	Layers:
	-	`sha256:5a600b153e3de53d31cba9f62f1af77ee9d6b8eb57c2db8aff3a8d426c07a84d`  
		Last Modified: Fri, 08 May 2026 19:22:16 GMT  
		Size: 2.2 MB (2241215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09b274effb57ce273ffe68124573b0dfba47ae490fe4c4bc52b7897af79955e7`  
		Last Modified: Fri, 08 May 2026 19:22:16 GMT  
		Size: 17.3 KB (17302 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - linux; 386

```console
$ docker pull julia@sha256:952cde523897d23a1c5f0d16d1586d8cd552a4e39ca1bd58f75ecffac7a211ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.1 MB (281059517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ffe74069f8b75adea501cb46bca6bc10b706f6adee5f01fda729544bdfd5a68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Fri, 01 May 2026 08:37:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 May 2026 08:37:26 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 01 May 2026 08:37:26 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 08:37:26 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 01 May 2026 08:37:26 GMT
ENV JULIA_VERSION=1.13.0-rc1
# Fri, 01 May 2026 08:37:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-rc1-linux-x86_64.tar.gz'; 			sha256='94c501d83aa46fad188894a31db093c6d065bbab94346645c775876066ec1b78'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-rc1-linux-i686.tar.gz'; 			sha256='1e758cfe0ba45a9b5313ff732ff5aa0d4f1927129e1b207e5e6c51e35ed9abb4'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-rc1-linux-aarch64.tar.gz'; 			sha256='0e08d6410e76a51b6825aed34c9e20fd5778b35cc4b406dd8eb8bd402d8df705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Fri, 01 May 2026 08:37:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 May 2026 08:37:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 May 2026 08:37:26 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:dacd7cda306bf5bd7a2030f9b0c2e9d71fda44ea58493a33450d210b74a8ec75`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 31.3 MB (31296327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9feb2f9a7a42d50aa0adb1a98ebc06fcdb0d3b4f9ce80dcf9c3773598abf8901`  
		Last Modified: Fri, 01 May 2026 08:38:02 GMT  
		Size: 6.4 MB (6433763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e817fa56028d606c912739f9d38a0317f0096e2a3ee0e7d8d2f217ecd394e07`  
		Last Modified: Fri, 01 May 2026 08:38:07 GMT  
		Size: 243.3 MB (243329054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace73a0ec1036dc601c1db9abe0bd878ab15528f2b30e4691a875ddc79781c2c`  
		Last Modified: Fri, 01 May 2026 08:38:02 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:7fd42cf6714465dd5816f0f46086795b7f8dea6b21cb4e613144bf5269a6204f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2255159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a268e692512800f4756b9d05895fcf7dd0c4f39151f4f8d7a444037fb80e9d1d`

```dockerfile
```

-	Layers:
	-	`sha256:505742e7d1e0d1e2c5e7c2a6e32aa801affb2f76fe1ce1a34be2b309ef2f2dfb`  
		Last Modified: Fri, 01 May 2026 08:38:02 GMT  
		Size: 2.2 MB (2238042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:434f8db0bdf19e63cf89669b85235e3b07de52b70738533251dd71a6b8ea87f0`  
		Last Modified: Fri, 01 May 2026 08:38:02 GMT  
		Size: 17.1 KB (17117 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - windows version 10.0.26100.32690; amd64

```console
$ docker pull julia@sha256:c590f899ed104cf6158eddf2eb78da0f3e5c102a9dff2dec786895065e804ff1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2442240085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5a9647855291ede84e16b8477842e75bf302cbf01b616283dcb92914f444ea0`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Fri, 01 May 2026 06:37:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 01 May 2026 06:37:01 GMT
ENV JULIA_VERSION=1.13.0-rc1
# Fri, 01 May 2026 06:37:02 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.13/julia-1.13.0-rc1-win64.exe
# Fri, 01 May 2026 06:37:03 GMT
ENV JULIA_SHA256=58e3b22f9e99b94f99bd81d26ca049ef1b4fd9aa0f58e7eb0d984f56cd76d4cf
# Fri, 01 May 2026 06:38:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 01 May 2026 06:38:51 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3642e4b8bb65ad3768f9f74a0dc48bb2e3294779b5d51573a234bfbe4f65324e`  
		Last Modified: Tue, 14 Apr 2026 18:48:19 GMT  
		Size: 606.9 MB (606926634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5a4a841b47f6d4734f84a9ffed102b568d8e2d220d024bfa81dc5aeda8a49d`  
		Last Modified: Fri, 01 May 2026 06:38:56 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be7c1fd979f6a35077064e62b96d99e70f140889855c4e8fb52b422ef12b1ec6`  
		Last Modified: Fri, 01 May 2026 06:38:55 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae0461eb154063a8ac7ab115f219831ed1a35a12e51977adf3ed4930f6456afa`  
		Last Modified: Fri, 01 May 2026 06:38:55 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad4ba19f31709312a8d90f582bbb24fc6fa4cd2936efd015c04b48f7f2c7f86a`  
		Last Modified: Fri, 01 May 2026 06:38:55 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfdf0d7e5784d994cd1084d5c6c9985054706b4d75fcbc53f3f78d3cc0fd1717`  
		Last Modified: Fri, 01 May 2026 06:39:41 GMT  
		Size: 312.2 MB (312247516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876c564356126a71e10b62ce8ff07af5cd2d6b6b80c97c4f51b36ac033003971`  
		Last Modified: Fri, 01 May 2026 06:38:55 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc` - windows version 10.0.20348.5020; amd64

```console
$ docker pull julia@sha256:401ad7585973d604032c1b9799a9a1fb852ed7811ab8526b4f38bcac9284c4ab
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2382523826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd18ce4a7e34a140a51c9b47b6d839f2eceaa1977ef7d0322f4d02a12204d02`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Fri, 01 May 2026 06:34:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 01 May 2026 06:34:35 GMT
ENV JULIA_VERSION=1.13.0-rc1
# Fri, 01 May 2026 06:34:36 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.13/julia-1.13.0-rc1-win64.exe
# Fri, 01 May 2026 06:34:36 GMT
ENV JULIA_SHA256=58e3b22f9e99b94f99bd81d26ca049ef1b4fd9aa0f58e7eb0d984f56cd76d4cf
# Fri, 01 May 2026 06:35:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 01 May 2026 06:35:50 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77be2f9c243b0e263c88ca2d726022040687be630dcf57393cc6b22b4185dbf`  
		Last Modified: Fri, 01 May 2026 06:36:00 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e932476babec9ee83f5a230f626301da45f76fac5cf900af2c2648cbfc2b5a`  
		Last Modified: Fri, 01 May 2026 06:35:58 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7a7358644a33dd8cff75bc9310d43243c6391a7112dcf15fd1ef85c3047e72`  
		Last Modified: Fri, 01 May 2026 06:35:58 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c14313f3dab02546408316191117d691fb0555f1bd46b60e37b44f496717d5`  
		Last Modified: Fri, 01 May 2026 06:35:58 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:383535af7e630d3f2db2832c2c8e141e0298958ab5dba981083f1c8091e4fe7d`  
		Last Modified: Fri, 01 May 2026 06:36:42 GMT  
		Size: 312.3 MB (312306104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3752c15d2e0e0040ccb2d4d90be4c5a921452d943fc6793c3f1336a82bc4f90`  
		Last Modified: Fri, 01 May 2026 06:35:58 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
