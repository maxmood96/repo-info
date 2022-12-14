## `openjdk:20-ea-jdk`

```console
$ docker pull openjdk@sha256:47fa838246cb192b29d4889373fe592e4c8722f6679a1d201528ad831abc5bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.20348.1366; amd64
	-	windows version 10.0.17763.3770; amd64

### `openjdk:20-ea-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:5fbcc562231e4121a2d7b9ad64b6d832a5f2cd722f13ded2f48f2fac2b308072
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.2 MB (254207156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e9dab371ace244284032c8b5078ce5c6518e462d841389763afb0e5b29fcfe`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 07 Dec 2022 01:51:27 GMT
ADD file:04d9ae26c2acac414b69a784563f765d531aeaf941ea0341025b4544f9ade244 in / 
# Wed, 07 Dec 2022 01:51:27 GMT
CMD ["/bin/bash"]
# Wed, 07 Dec 2022 02:27:04 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 07 Dec 2022 02:27:04 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Wed, 07 Dec 2022 02:27:04 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Dec 2022 02:27:04 GMT
ENV LANG=C.UTF-8
# Mon, 12 Dec 2022 20:57:39 GMT
ENV JAVA_VERSION=20-ea+27
# Mon, 12 Dec 2022 20:57:50 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/27/GPL/openjdk-20-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='fc3bc8e77b3b556d06a55cf2c2e5510c94359858d5c691b38575aa164eade92b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/27/GPL/openjdk-20-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='7828ad1bee0c3e813c02057353eca047c86f3799cfe3c76cbe21b15d57b239bb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 12 Dec 2022 20:57:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0ed027b72ddc5d1a749fc58b7c26610167393b08ae71ef6625496508903f70a2`  
		Last Modified: Wed, 07 Dec 2022 01:53:11 GMT  
		Size: 43.9 MB (43868738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3502f40d35be69b4df858d92b5ac60d6b792eec7beabb7cbd78c816329f47b7f`  
		Last Modified: Wed, 07 Dec 2022 02:30:44 GMT  
		Size: 12.2 MB (12248357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad92a17effe7907e4c4a0cc1c998ba13d56d0f9aa560a882b154676a2fdef23`  
		Last Modified: Mon, 12 Dec 2022 21:01:50 GMT  
		Size: 198.1 MB (198090061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:772747591c995eec9c96708c16d3d705a77fdf9e63696569cf4b581ff525ee48
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.4 MB (252410683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4f56c5c9ec056f45daccced9a84fe9bb946715b75b0d409399089fe7502aa15`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 07 Dec 2022 02:10:44 GMT
ADD file:6fdd782c2779edf7149126e79dcb46ebde32975107cdd5d129cce0860e797cde in / 
# Wed, 07 Dec 2022 02:10:44 GMT
CMD ["/bin/bash"]
# Wed, 07 Dec 2022 02:53:05 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 07 Dec 2022 02:53:05 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Wed, 07 Dec 2022 02:53:06 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Dec 2022 02:53:06 GMT
ENV LANG=C.UTF-8
# Mon, 12 Dec 2022 19:53:16 GMT
ENV JAVA_VERSION=20-ea+27
# Mon, 12 Dec 2022 19:53:26 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/27/GPL/openjdk-20-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='fc3bc8e77b3b556d06a55cf2c2e5510c94359858d5c691b38575aa164eade92b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/27/GPL/openjdk-20-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='7828ad1bee0c3e813c02057353eca047c86f3799cfe3c76cbe21b15d57b239bb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 12 Dec 2022 19:53:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:12a06ca91af857ea3cb02aedc5c643c5f06865868ae5c386c8ea664be60ead7e`  
		Last Modified: Wed, 07 Dec 2022 02:12:09 GMT  
		Size: 42.8 MB (42772059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122e459b46a4edc515fedc5c9be076b28ba6b0606f3cc90d412ea3d88b15576e`  
		Last Modified: Wed, 07 Dec 2022 02:57:10 GMT  
		Size: 13.1 MB (13058882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ad25abcf887203842aca2b67bd35274a7cd2dea52f633a4a3e66bf9464c2c6`  
		Last Modified: Mon, 12 Dec 2022 19:57:41 GMT  
		Size: 196.6 MB (196579742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-jdk` - windows version 10.0.20348.1366; amd64

```console
$ docker pull openjdk@sha256:9e9f3efd351639c2c54d46eb8bb7739c444b09c809615dcee334528f3fa7326f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2690324736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be28271c0d923093bc322c3e0d56c57d12ee3a45662925a7c94b2d3ceae7f53d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Fri, 09 Dec 2022 09:36:47 GMT
RUN Install update 10.0.20348.1366
# Tue, 13 Dec 2022 22:45:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Dec 2022 02:49:23 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 14 Dec 2022 02:59:12 GMT
ENV JAVA_HOME=C:\openjdk-20
# Wed, 14 Dec 2022 03:00:28 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 14 Dec 2022 03:00:29 GMT
ENV JAVA_VERSION=20-ea+27
# Wed, 14 Dec 2022 03:00:30 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk20/27/GPL/openjdk-20-ea+27_windows-x64_bin.zip
# Wed, 14 Dec 2022 03:00:31 GMT
ENV JAVA_SHA256=115761fb06b9bf09bd9b174d80cf45d45ace29e92a50742af53ff02cb63088d2
# Wed, 14 Dec 2022 03:01:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 14 Dec 2022 03:01:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a4aee932fccc1ec8135f290aca03a7c93dcc2536fc84723813ef9b95f6fd13ea`  
		Last Modified: Wed, 18 May 2022 07:59:24 GMT  
		Size: 1.5 GB (1473997635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bfa20ce142ecceb471dc070d9582fff942cef447b7c8ff22f2223ffe3737c99`  
		Last Modified: Tue, 13 Dec 2022 23:54:14 GMT  
		Size: 1.0 GB (1021665190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb8b9a4ec3ca516cfaa44f64e80b1e3aaecdbde870177411ff046f81f991dd2`  
		Last Modified: Tue, 13 Dec 2022 23:51:33 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc6d0e6b431095ccd3ac842154ae597a56b82834441570a9c95689f517a56ea`  
		Last Modified: Wed, 14 Dec 2022 08:45:36 GMT  
		Size: 576.9 KB (576869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4228fff1ac4aaf864043ab6ff5341b37ddfbd89a849a638653c590e869dbfa6`  
		Last Modified: Wed, 14 Dec 2022 08:47:59 GMT  
		Size: 1.4 KB (1450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7713d48cae58aee42cae5f4e53713018d24ab93530ff940fdadfcfba60393b9`  
		Last Modified: Wed, 14 Dec 2022 08:48:00 GMT  
		Size: 512.9 KB (512898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0768654e58eece503fb1a3566149c0d8e5363bb7c47abeb9b1eb79be12e04b2`  
		Last Modified: Wed, 14 Dec 2022 08:47:57 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2323e89565daed05c5656bcca56935f8ef85a8bf921c3c75c5866f1d51f6a189`  
		Last Modified: Wed, 14 Dec 2022 08:47:57 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d41a4a8c7b8dc8340acdfcb17ca52beec80e610fbaee3a8a4aa78d08e995904`  
		Last Modified: Wed, 14 Dec 2022 08:47:57 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:433cd8ebbe7a918e51df6091b6d3477aff1d2f312cf54a40ac18923430281490`  
		Last Modified: Wed, 14 Dec 2022 08:48:25 GMT  
		Size: 193.6 MB (193563554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca08f1524994832067b5f2bb848322256ff11df4a4997ece5725ddacf02e45d`  
		Last Modified: Wed, 14 Dec 2022 08:47:57 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-jdk` - windows version 10.0.17763.3770; amd64

```console
$ docker pull openjdk@sha256:f9e5d27900ea61e6234a5ed061f940124b7cb813516e9df2c47974923d1603e5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2974739730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70888e5b7cead24baa6c104eefb7a1daa1ee4011776ff0575db8b77d772b3746`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sun, 11 Dec 2022 08:04:49 GMT
RUN Install update 10.0.17763.3770
# Tue, 13 Dec 2022 22:48:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Dec 2022 02:52:45 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 14 Dec 2022 03:01:57 GMT
ENV JAVA_HOME=C:\openjdk-20
# Wed, 14 Dec 2022 03:03:46 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 14 Dec 2022 03:03:47 GMT
ENV JAVA_VERSION=20-ea+27
# Wed, 14 Dec 2022 03:03:47 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk20/27/GPL/openjdk-20-ea+27_windows-x64_bin.zip
# Wed, 14 Dec 2022 03:03:48 GMT
ENV JAVA_SHA256=115761fb06b9bf09bd9b174d80cf45d45ace29e92a50742af53ff02cb63088d2
# Wed, 14 Dec 2022 03:06:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 14 Dec 2022 03:06:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3ad73ed772f80ab7923579a55dd12fb9b6e090d1d836408d16ffd9d3dee252`  
		Last Modified: Tue, 13 Dec 2022 23:56:47 GMT  
		Size: 856.4 MB (856427878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc9debb9503ac53c2f64685982eca56ac5110ea6baf7278b27af54ab8fbc409`  
		Last Modified: Tue, 13 Dec 2022 23:54:25 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e607bf43cbd414b2f7d5b6fdfc84e9eb56c2552fe9826cffa690a9d1fd381c`  
		Last Modified: Wed, 14 Dec 2022 08:46:21 GMT  
		Size: 348.4 KB (348396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e03c14bc9e3d2e4c1490e4b54ba16c12f364ecbabdde8bca9ef0491c8a6398`  
		Last Modified: Wed, 14 Dec 2022 08:48:45 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a4c3c241bec90807320674aa89214b5b5dee32c495417743ff949d6c9127020`  
		Last Modified: Wed, 14 Dec 2022 08:48:45 GMT  
		Size: 309.9 KB (309875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:861b22bd3383eabf591db7d1801166dec2c7417541eb8edd26319f6bcb02f031`  
		Last Modified: Wed, 14 Dec 2022 08:48:43 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c70827509905ab79454773a5658f693ab2bdfd33da421e16b5386ce1f6e5690`  
		Last Modified: Wed, 14 Dec 2022 08:48:43 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c648fb0a9d3943f7eb6e607c42454fd77e2dd6f6e16d44d97d7ac471a5c94c1f`  
		Last Modified: Wed, 14 Dec 2022 08:48:43 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffc64fb29c71e2e1ebd7bbdf3d264aa48bb7c2119811ac810740d051fccd647`  
		Last Modified: Wed, 14 Dec 2022 08:49:05 GMT  
		Size: 193.4 MB (193375658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebba3333eb5494133b11d0321c2a3e2351b86bf1233f2740361e465089e21403`  
		Last Modified: Wed, 14 Dec 2022 08:48:43 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
