## `openjdk:19-ea-15-jdk`

```console
$ docker pull openjdk@sha256:e9f335d844787fe01ded1e4217fea38701ddb00c4237e41aa5ccebf38e140845
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.20348.587; amd64
	-	windows version 10.0.17763.2686; amd64

### `openjdk:19-ea-15-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:c3adcf293e562de010bb63d5a42b242630490bb0a16c35fa2945a95e675b0994
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.8 MB (248841182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69e157ef5b874585dfe38af77ada230434b0d0015606e2f0931c59fcba4cf4bf`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 24 Mar 2022 22:26:17 GMT
ADD file:ebb4986af4fcca0d00738e77d2c814e70536c01a0e02eef98c71e9e3a56c0abd in / 
# Thu, 24 Mar 2022 22:26:18 GMT
CMD ["/bin/bash"]
# Fri, 25 Mar 2022 01:16:47 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 25 Mar 2022 01:16:47 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Fri, 25 Mar 2022 01:16:47 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Mar 2022 01:16:47 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 00:51:23 GMT
ENV JAVA_VERSION=19-ea+15
# Tue, 29 Mar 2022 00:51:35 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/15/GPL/openjdk-19-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='ac2dedbf7805d85112f20815eb381e1fec51c9d1057f6c0eaf1185ca9c1b2c5e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/15/GPL/openjdk-19-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='039c2cdec816ea3afe5430f2b9bc74749b10b3372894a9d4098eabef60492a3c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 29 Mar 2022 00:51:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1de6f411eccf5041d90362d2d035abf0e59cf91dce4eacbc37ef0aa52f5b5920`  
		Last Modified: Thu, 24 Mar 2022 22:27:23 GMT  
		Size: 42.1 MB (42111629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fbc239737191ccc9950c0b7c7a0aa6dac0a92906c45c8c72d511820cf4cd3b6`  
		Last Modified: Fri, 25 Mar 2022 01:24:51 GMT  
		Size: 13.5 MB (13530268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64458ab0f171b4f00c71c3d97205f7d23d50b4972f98ed2a5beb2c2fc8e13e6d`  
		Last Modified: Tue, 29 Mar 2022 01:02:48 GMT  
		Size: 193.2 MB (193199285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-ea-15-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:3ed8dc88c4683e019627226704c0c23d14018e3de59f1c35d58f0a5dc0397fe5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.4 MB (248396693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f6f901739d6bc4e497f2312296fd8ba01a235738270465e2ac3a9e6ac5e05a`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 24 Mar 2022 22:21:09 GMT
ADD file:1eaca9dccdbe88c4fac0b484a625100443af30879cf6cba7b5615db77745b0c7 in / 
# Thu, 24 Mar 2022 22:21:10 GMT
CMD ["/bin/bash"]
# Thu, 24 Mar 2022 22:45:15 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 24 Mar 2022 22:45:16 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Thu, 24 Mar 2022 22:45:17 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Mar 2022 22:45:18 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 01:16:33 GMT
ENV JAVA_VERSION=19-ea+15
# Tue, 29 Mar 2022 01:16:50 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/15/GPL/openjdk-19-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='ac2dedbf7805d85112f20815eb381e1fec51c9d1057f6c0eaf1185ca9c1b2c5e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/15/GPL/openjdk-19-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='039c2cdec816ea3afe5430f2b9bc74749b10b3372894a9d4098eabef60492a3c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 29 Mar 2022 01:16:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c11319b13f376dfb3fa1ee22d0047cfb7157eba4ba2786653cb29ac6defcb93c`  
		Last Modified: Thu, 24 Mar 2022 22:22:26 GMT  
		Size: 42.0 MB (42018948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d7710250d8de942c9ab085f8642e5e854d0b85b2578079aa2a8f4aaac0bf73`  
		Last Modified: Thu, 24 Mar 2022 23:01:12 GMT  
		Size: 14.3 MB (14293656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9efe9ab413014049e6eb2e57f29ee6aea9d39fba47a35abd2c01a21b9817b969`  
		Last Modified: Tue, 29 Mar 2022 01:35:52 GMT  
		Size: 192.1 MB (192084089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-ea-15-jdk` - windows version 10.0.20348.587; amd64

```console
$ docker pull openjdk@sha256:01bd531aa70eec0f75a65446522667a762c58fa3a024c1e60b407a603b4e2095
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2410728176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:975eafa0d3a59f49d6ca395837b5b4e5b1770598d7efd37df98d36c02f3fa031`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Thu, 03 Mar 2022 05:02:11 GMT
RUN Install update ltsc2022-amd64
# Tue, 08 Mar 2022 19:26:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 17:08:43 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 09 Mar 2022 17:08:44 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 09 Mar 2022 17:09:03 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 29 Mar 2022 00:15:39 GMT
ENV JAVA_VERSION=19-ea+15
# Tue, 29 Mar 2022 00:15:40 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk19/15/GPL/openjdk-19-ea+15_windows-x64_bin.zip
# Tue, 29 Mar 2022 00:15:41 GMT
ENV JAVA_SHA256=f370eecd71ab1f5349c78c0bb82516c49fb4635790c895e11bca04ce2d5bbb4c
# Tue, 29 Mar 2022 00:16:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 29 Mar 2022 00:16:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:037d5740b40414bc505c21324142a1cd3eab10c176189a9a74d1a90354ac7cd4`  
		Size: 969.5 MB (969547968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d58ba398110c3f761c6307a5621ec218b8593ba8b07b734436bcdd8d07a23e08`  
		Last Modified: Tue, 08 Mar 2022 20:00:31 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536e5c64699fc55f528fe9ed2ca2c4088a1b329a50236ef20b400958daadc725`  
		Last Modified: Wed, 09 Mar 2022 17:40:56 GMT  
		Size: 600.0 KB (600021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:242a279bb38e5c0949759b401e7be86d7f899c9457fba0eeabdef0fec92f6682`  
		Last Modified: Wed, 09 Mar 2022 17:40:55 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f4c6cacc278c66995aee924b612b9af7a269c23ba83a9f7d62e975c98e167f`  
		Last Modified: Wed, 09 Mar 2022 17:40:56 GMT  
		Size: 510.3 KB (510254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83101e0f3048f6c4c8f87c15f7aa8ffdd69712614941382a20a8aede5d6f7497`  
		Last Modified: Tue, 29 Mar 2022 00:25:05 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ff809e4f72dac731c047fa7e6396b596a52f9e4e3e790a8378183fe6c87b82`  
		Last Modified: Tue, 29 Mar 2022 00:25:05 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01aa5e9d11b89862a8682dc6a9f4549713d97dc6740e70f89614afb7acf068b`  
		Last Modified: Tue, 29 Mar 2022 00:25:05 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d0a7dacbcdc0ad8159dd22b53b8e8604c5aa49d3509439c4ec812f2d03f985`  
		Last Modified: Tue, 29 Mar 2022 00:28:27 GMT  
		Size: 188.4 MB (188362384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519c72e75c0009a63112435e695714144edc13d830dd7af03f5e327e22e3fa40`  
		Last Modified: Tue, 29 Mar 2022 00:25:05 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-ea-15-jdk` - windows version 10.0.17763.2686; amd64

```console
$ docker pull openjdk@sha256:7676bf841fc46984ac1ee59170f4e4a386ac357fa9a6f79f93553e79b701f18c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2904303121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f58645f6c869aef2b11dcc16e5e5e52e0ae915b0a74dc8d3bed9b871cf0977d1`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 17:11:03 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 09 Mar 2022 17:11:04 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 09 Mar 2022 17:11:56 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 29 Mar 2022 00:16:52 GMT
ENV JAVA_VERSION=19-ea+15
# Tue, 29 Mar 2022 00:16:53 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk19/15/GPL/openjdk-19-ea+15_windows-x64_bin.zip
# Tue, 29 Mar 2022 00:16:54 GMT
ENV JAVA_SHA256=f370eecd71ab1f5349c78c0bb82516c49fb4635790c895e11bca04ce2d5bbb4c
# Tue, 29 Mar 2022 00:18:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 29 Mar 2022 00:18:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:082ea46951b109a477871d3f8739d105427abdbef68b50e54b54b4ed440f48e8`  
		Last Modified: Wed, 09 Mar 2022 17:41:38 GMT  
		Size: 356.5 KB (356505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c303714362d4354175bfbd60bde4487fb5663326536432755fabbeca5237db`  
		Last Modified: Wed, 09 Mar 2022 17:41:37 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ced75f82f0e7f243af02f1c1abe1b9baafcfd9b31f208d60f85f675e0fb5c1`  
		Last Modified: Wed, 09 Mar 2022 17:41:37 GMT  
		Size: 310.2 KB (310174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81dbdfb3b33d9b68a92f9ba8e467d1379ea06450f83a04247d0a31000af009fa`  
		Last Modified: Tue, 29 Mar 2022 00:28:49 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99ae52e520dbbb5826bc09183c7309c35d2af7a5836df8649b453c9b6ea196aa`  
		Last Modified: Tue, 29 Mar 2022 00:28:49 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c60a87586267e0e1dd5a340edbc45d28827e900ed8d80a7165d17b0a2213a56`  
		Last Modified: Tue, 29 Mar 2022 00:28:49 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd6096eb320a89b45c5dc27111a8f7ccdc57a35d56e8f3e503158e174902c17`  
		Last Modified: Tue, 29 Mar 2022 00:29:08 GMT  
		Size: 188.2 MB (188175390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c645e70d8cec362c49bf92be71bd4971a6420f8960a4c9ec2281e4b40052f8`  
		Last Modified: Tue, 29 Mar 2022 00:28:49 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
