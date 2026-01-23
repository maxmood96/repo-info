## `openjdk:27-ea-5-jdk`

```console
$ docker pull openjdk@sha256:6e993acb8a48394c7bcbda4137d609e0d7f931a3c6f0e14fc1efe8fddeb4db39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `openjdk:27-ea-5-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:3db54cd179fcb0bf8e6a0feea230837dfe9f2cd58f01266ac4f2098cf2eb195c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.7 MB (313676708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ee2cf868ebae36261d7a0aca63c878e23d9db4d291a38f33de84b91754cad19`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 23 Jan 2026 00:58:01 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:58:01 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:07:18 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:07:29 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Fri, 23 Jan 2026 01:07:29 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jan 2026 01:07:29 GMT
ENV LANG=C.UTF-8
# Fri, 23 Jan 2026 01:07:29 GMT
ENV JAVA_VERSION=27-ea+5
# Fri, 23 Jan 2026 01:07:29 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/5/GPL/openjdk-27-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='2d85f5a6432abd2eb67b974ed1ab85d2a9557b06be285f2fc6e5d94429951468'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/5/GPL/openjdk-27-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='58f4450fff4f277000cf3d520a612275b0d9b6cb24e1287457d4651e98714b4a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 23 Jan 2026 01:07:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:16506d4b4233ebc21b62f7593851ebfe31dec192fdb790c8c857eca6260f7a57`  
		Last Modified: Fri, 23 Jan 2026 00:58:12 GMT  
		Size: 47.3 MB (47313548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effa302177a5c6a5c4dc88c1937c3c5c7de7276be4f52c4996088f50c84385ce`  
		Last Modified: Fri, 23 Jan 2026 01:07:53 GMT  
		Size: 38.3 MB (38296652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd842e7a994931dc439ba3fc0bbc8a95e49421be8273ebc3c9e7a617571ed4d2`  
		Last Modified: Fri, 23 Jan 2026 01:07:56 GMT  
		Size: 228.1 MB (228066508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-5-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:fbdc4bf55a61fea5add42e6cfdf4e6a0c6b6272c5992d822962b71d3d842c30c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01e7e4b9a1129a27517bface44e44b57d1ce4c5147aa184e3960fd9d5730233d`

```dockerfile
```

-	Layers:
	-	`sha256:ac4844cd89b038c90c22cac52fa0f9d2c21d15150a4350852542cf7fe6d9524d`  
		Last Modified: Fri, 23 Jan 2026 01:07:51 GMT  
		Size: 3.7 MB (3655359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e690c27bb6dd30d06bea702cc2f7f2d99fea44325180b820f10aa2538f376d08`  
		Last Modified: Fri, 23 Jan 2026 01:07:51 GMT  
		Size: 17.8 KB (17814 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-5-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:eb9e9b3614aa388d392616143983edbaf157e1c7839bd8db41709bd44d6e2e13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310601155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80631cad885568c01fdd5ddba1779c52e9d9cd69fefb12532ed3e54a37d3cf17`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 23 Jan 2026 00:57:45 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:57:45 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:02:39 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:57 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Fri, 23 Jan 2026 01:03:57 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jan 2026 01:03:57 GMT
ENV LANG=C.UTF-8
# Fri, 23 Jan 2026 01:03:57 GMT
ENV JAVA_VERSION=27-ea+5
# Fri, 23 Jan 2026 01:03:57 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/5/GPL/openjdk-27-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='2d85f5a6432abd2eb67b974ed1ab85d2a9557b06be285f2fc6e5d94429951468'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/5/GPL/openjdk-27-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='58f4450fff4f277000cf3d520a612275b0d9b6cb24e1287457d4651e98714b4a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 23 Jan 2026 01:03:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cb58e3477df4a511e30cc2dda04665dfc7b948e198e587c0ae4203a6cd829165`  
		Last Modified: Fri, 23 Jan 2026 00:57:57 GMT  
		Size: 45.9 MB (45901910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b714d6dc4abe6f689665354c4cf44a16e94729cfc60fabd29fa1982418eb96d`  
		Last Modified: Fri, 23 Jan 2026 01:04:19 GMT  
		Size: 38.7 MB (38699722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672a88aee01418c9d2646f5349ccc80b1e6b94bf8d3d6a763f99012af309b381`  
		Last Modified: Fri, 23 Jan 2026 01:04:23 GMT  
		Size: 226.0 MB (225999523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-5-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:b2d65aafc757a4dc865f886aaaecac7a3c53326a908bb3b6f93b538c44a4fe43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b61cb31f7f4e2406725f2c57a0e3abf36a1557d5dd9614905a08acf08b6aef4`

```dockerfile
```

-	Layers:
	-	`sha256:dcaee0da90de3e973149623f94dbfa8d162c3656b0b10f7e604b761831ec312d`  
		Last Modified: Fri, 23 Jan 2026 01:04:18 GMT  
		Size: 3.7 MB (3653049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab2ca04b5980b5bd83d52e22509aa798a3e15ae1ed580b145fc0dcf9111300bb`  
		Last Modified: Fri, 23 Jan 2026 01:04:18 GMT  
		Size: 18.0 KB (18029 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-5-jdk` - windows version 10.0.26100.32230; amd64

```console
$ docker pull openjdk@sha256:abcb36b51d04b6571e9c56bfa42c5e4594f5f5a770ff5fbfc3bc10f55fdb6d30
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1721044983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d02002222aa11bed971aa6b711f9fe66b1e736021d0df5887a9668eeab2a6af`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 20 Jan 2026 18:51:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 20 Jan 2026 18:51:59 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 20 Jan 2026 18:52:00 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 20 Jan 2026 18:52:06 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 20 Jan 2026 18:52:07 GMT
ENV JAVA_VERSION=27-ea+5
# Tue, 20 Jan 2026 18:52:08 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/5/GPL/openjdk-27-ea+5_windows-x64_bin.zip
# Tue, 20 Jan 2026 18:52:09 GMT
ENV JAVA_SHA256=350ca51cd4321274f6557de42448fd4fc6e845cfe0695800868857f13f89a2fc
# Tue, 20 Jan 2026 18:52:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 20 Jan 2026 18:52:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e72e4b6e32077245586401d96dcbe5dfbfc76b2346166f48cdcfa0df93664650`  
		Last Modified: Tue, 20 Jan 2026 18:52:45 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662149f580d6da5f5f5954a737745aa3ec95b0e3b53799353b7da0257fd4a467`  
		Last Modified: Tue, 20 Jan 2026 18:52:45 GMT  
		Size: 403.4 KB (403418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46759ad4730fb651350be3a6af1de57ca13252b75fb154da903a6887b4a44ff`  
		Last Modified: Tue, 20 Jan 2026 18:52:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843be8db1e5bd4fba522492479b13fb0d3a1fd4bdabd1dea8d4c85ce8481c74e`  
		Last Modified: Tue, 20 Jan 2026 18:52:45 GMT  
		Size: 388.6 KB (388563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a2ea9fbd7e89bcdafe59e0fea26fec21cd3b2776079541fc936fa20a89a547`  
		Last Modified: Tue, 20 Jan 2026 18:52:43 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d009c75f850597872b10e10fa558a19241c9906960ee9d46b8761280f0c82f83`  
		Last Modified: Tue, 20 Jan 2026 18:52:43 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffde2380cd4e2a2a84fed9cab589e7ff1aef81e6b2643b5e9ff3988ad65f20b`  
		Last Modified: Tue, 20 Jan 2026 18:52:44 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465155860de126dae51438501c5c5846510546dd52a805ca574cbcc72c6d48c2`  
		Last Modified: Tue, 20 Jan 2026 18:53:00 GMT  
		Size: 224.5 MB (224484872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e494abfcc7bbb7bc54757d0f4b6c94dbe340549658e352c24a3425cea7e8aa24`  
		Last Modified: Tue, 20 Jan 2026 18:52:43 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-5-jdk` - windows version 10.0.20348.4648; amd64

```console
$ docker pull openjdk@sha256:36f4ca3dbb5838e1bd200eee72c5ea9460157364de3edd95a48ffcb466c77a3d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2061004440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:983bb2d518ed2afd1c8e299edd57e7849f0b69231b79c051bc6f14b818c56a35`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 20 Jan 2026 18:54:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 20 Jan 2026 18:55:58 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 20 Jan 2026 18:55:59 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 20 Jan 2026 18:56:06 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 20 Jan 2026 18:56:07 GMT
ENV JAVA_VERSION=27-ea+5
# Tue, 20 Jan 2026 18:56:08 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/5/GPL/openjdk-27-ea+5_windows-x64_bin.zip
# Tue, 20 Jan 2026 18:56:10 GMT
ENV JAVA_SHA256=350ca51cd4321274f6557de42448fd4fc6e845cfe0695800868857f13f89a2fc
# Tue, 20 Jan 2026 18:56:44 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 20 Jan 2026 18:56:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12503e819e94357068d715ad8ecf83f339bd5889b12d224bfd56b14fc18ed03`  
		Last Modified: Tue, 20 Jan 2026 18:56:52 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3734874d8df4d7d771d6b1069ee7161637b1c85f22f98b4159d6b88d52986f32`  
		Last Modified: Tue, 20 Jan 2026 18:56:52 GMT  
		Size: 513.0 KB (512968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a40ed685c42672d72a2ca56606735d97bbb3e73fb3efffd84f5dc98f83175c`  
		Last Modified: Tue, 20 Jan 2026 18:56:52 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d298107636bc92dd10715ab2e90da677425c7ef68a7ee07eb9ca510adf2958`  
		Last Modified: Tue, 20 Jan 2026 18:56:52 GMT  
		Size: 360.2 KB (360169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286b4060bec13e685f9eabab1eb4aac12f72419b9a03cc08e06d8721eca263e9`  
		Last Modified: Tue, 20 Jan 2026 18:56:51 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a2735f865a5901c5e0d56b5c640cca88ed7a07e5be27a93ff7cf9dd6362b91`  
		Last Modified: Tue, 20 Jan 2026 18:56:51 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf5658709f37c40a3845d61f68860c77c7d902a98f5c2909661d2568c4b3f58`  
		Last Modified: Tue, 20 Jan 2026 18:56:51 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21bd7fe4f4bae5fc8e5338fddc1e340eadb8313fbb3e3038c89d4e544e288765`  
		Last Modified: Tue, 20 Jan 2026 18:57:06 GMT  
		Size: 224.5 MB (224464285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6cecd6b7b9ff1f44fcab2283976b2e06e2c9218eb6f1e613530da7e757264b`  
		Last Modified: Tue, 20 Jan 2026 18:56:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
