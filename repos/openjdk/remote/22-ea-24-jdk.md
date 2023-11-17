## `openjdk:22-ea-24-jdk`

```console
$ docker pull openjdk@sha256:4a0df9390f200cb077e4470afb8f8491e932e61b84a6a786f63457a717891cf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.20348.2113; amd64
	-	windows version 10.0.17763.5122; amd64

### `openjdk:22-ea-24-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:77da5d2cd95cde7b6eb64964720361b62b86200f185230222864f03c4ee8603d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.6 MB (263550531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57acad158cfba56809cb79c3e536b0a32b5ef572573c1b6278623b943bfb660b`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 20 Oct 2023 18:27:20 GMT
ADD file:0f45bdf93b14a2ab9389b71d23b6c7f6d2935c8016e3b6422814f8fc79bef986 in / 
# Fri, 20 Oct 2023 18:27:20 GMT
CMD ["/bin/bash"]
# Fri, 20 Oct 2023 18:45:06 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 20 Oct 2023 18:45:06 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Fri, 20 Oct 2023 18:45:06 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Oct 2023 18:45:06 GMT
ENV LANG=C.UTF-8
# Fri, 17 Nov 2023 04:28:36 GMT
ENV JAVA_VERSION=22-ea+24
# Fri, 17 Nov 2023 04:28:55 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/24/GPL/openjdk-22-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='f2b3d5371bc7ab762205f286fc5b5da9dabbdd0477965fc87d02076faf69ab3a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/24/GPL/openjdk-22-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='909c2841030baff026a45248785f3dc50906ce921620913a28b8d6cca0075838'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 17 Nov 2023 04:28:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8e0176adc18c476bdfcc701f01cda5acf49bc8e6d7fadac8072091a43fafbb25`  
		Last Modified: Fri, 20 Oct 2023 18:28:56 GMT  
		Size: 44.3 MB (44279620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e7fcefe71b24cef619772a3adab6474d1dee79d5ec55a8ac900504be9b669d3`  
		Last Modified: Fri, 20 Oct 2023 18:46:04 GMT  
		Size: 15.0 MB (15016123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0cf99a9d69e9eba77b52b5be6e121bfbe32b0ce0851ff8f84f4d0a718dd502`  
		Last Modified: Fri, 17 Nov 2023 04:31:53 GMT  
		Size: 204.3 MB (204254788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-24-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:d379c3ab300011486210731b10be1f1e2eea546a051b6f92e6658f17d9931261
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261647253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6838fb340d924a39b46cc997589d0b3be1396a89a36f2c135faac7bc8804e29e`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 20 Oct 2023 18:39:12 GMT
ADD file:e189ba41c54c386435a3292026b75a1386976d3222102c16a725f58f594f284e in / 
# Fri, 20 Oct 2023 18:39:12 GMT
CMD ["/bin/bash"]
# Fri, 20 Oct 2023 19:20:37 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 20 Oct 2023 19:20:38 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Fri, 20 Oct 2023 19:20:38 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Oct 2023 19:20:38 GMT
ENV LANG=C.UTF-8
# Fri, 17 Nov 2023 02:04:44 GMT
ENV JAVA_VERSION=22-ea+24
# Fri, 17 Nov 2023 02:05:07 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/24/GPL/openjdk-22-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='f2b3d5371bc7ab762205f286fc5b5da9dabbdd0477965fc87d02076faf69ab3a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/24/GPL/openjdk-22-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='909c2841030baff026a45248785f3dc50906ce921620913a28b8d6cca0075838'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 17 Nov 2023 02:05:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e39ec8f010eb75816ae2c21b014f7fdecffb48374079b6f1bce017214e2a45cd`  
		Last Modified: Fri, 20 Oct 2023 18:40:29 GMT  
		Size: 43.7 MB (43672784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa4910a471f6760b5f0bc0ef155e7afd624a4c1ea6f09bb680d43c1041cfd4fd`  
		Last Modified: Fri, 20 Oct 2023 19:21:34 GMT  
		Size: 15.7 MB (15660393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cc90748a7c7b76ab586f2f07f6f493aae771b025656dd0dd7826a57c46427d`  
		Last Modified: Fri, 17 Nov 2023 02:08:23 GMT  
		Size: 202.3 MB (202314076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-24-jdk` - windows version 10.0.20348.2113; amd64

```console
$ docker pull openjdk@sha256:51d3439e33bed6b403241a82f80dd469c397a6d42c88675423bed9b32de33cbc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2086714072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3149ad69a2eb742bfdc896ad25eeae7eb059c11a4f618fe3dca222de2ad853f5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 09 Nov 2023 06:47:20 GMT
RUN Install update 10.0.20348.2113
# Thu, 16 Nov 2023 01:36:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Nov 2023 05:18:36 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 16 Nov 2023 05:18:37 GMT
ENV JAVA_HOME=C:\openjdk-22
# Thu, 16 Nov 2023 05:18:57 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 17 Nov 2023 02:15:55 GMT
ENV JAVA_VERSION=22-ea+24
# Fri, 17 Nov 2023 02:15:56 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/24/GPL/openjdk-22-ea+24_windows-x64_bin.zip
# Fri, 17 Nov 2023 02:15:57 GMT
ENV JAVA_SHA256=13f049664a66ebfa61bb0fe3f04e3d09c6778a57feac8d2f6a8453bd29358f87
# Fri, 17 Nov 2023 02:16:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 17 Nov 2023 02:16:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7989ef2c4cfb06d845746a3c3660481ea84d3f5c8216041855ce528f0ac4015c`  
		Last Modified: Tue, 14 Nov 2023 20:43:13 GMT  
		Size: 498.2 MB (498182566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbeb193d02c2ca7f9a9ea438fbf1bcdb6ea4a6fea626713330fd1ebb514424f`  
		Last Modified: Thu, 16 Nov 2023 02:25:14 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c484d21f80984bc956d2a7ca187c7250676fd3af73a362efb91125bb6255aa10`  
		Last Modified: Thu, 16 Nov 2023 05:26:11 GMT  
		Size: 453.2 KB (453223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eaf9eb81e5d07980ecf0f7d31f640ebd53980837baa8588ca770fa56963edd6`  
		Last Modified: Thu, 16 Nov 2023 05:26:11 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be91ce40f73c6eaafd338b1fc738f4394dc6542fd074fc12e651a47dfd49e6f3`  
		Last Modified: Thu, 16 Nov 2023 05:26:11 GMT  
		Size: 263.4 KB (263380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55e09490ec346d2e1398dca0b2490d0c3aa5ddfb25b46895ab630fdcd2a7280a`  
		Last Modified: Fri, 17 Nov 2023 02:20:23 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01352a06a9a2c703d70af01a1b113aafd2aa9d083e79550e42ca0388c19a3df0`  
		Last Modified: Fri, 17 Nov 2023 02:20:23 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6706e9be5ca5f1f038d2a8f73a523c932117fd91dbc8499666c4f8c5d3d75e6`  
		Last Modified: Fri, 17 Nov 2023 02:20:23 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2a29b065d599bfb5061cae85cd8463eedd695df41e74ae02e97a026a3ecbccf`  
		Last Modified: Fri, 17 Nov 2023 02:20:43 GMT  
		Size: 199.2 MB (199207951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b3eb2668ccb33ff1f244e42720c1d237474d70982b16f2b7cbd19b308b1f43`  
		Last Modified: Fri, 17 Nov 2023 02:20:24 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-24-jdk` - windows version 10.0.17763.5122; amd64

```console
$ docker pull openjdk@sha256:e649d2aa6a4729598fa76e709ccee3d0849b2f42b3eec1a86dedbae22203cc2e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2257354381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d0ca41e7e385e48e6a3408d448749091d555fee69a9bd434c2abde58276770d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 01:37:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Nov 2023 05:21:26 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 16 Nov 2023 05:21:27 GMT
ENV JAVA_HOME=C:\openjdk-22
# Thu, 16 Nov 2023 05:22:38 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 17 Nov 2023 02:17:10 GMT
ENV JAVA_VERSION=22-ea+24
# Fri, 17 Nov 2023 02:17:12 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/24/GPL/openjdk-22-ea+24_windows-x64_bin.zip
# Fri, 17 Nov 2023 02:17:13 GMT
ENV JAVA_SHA256=13f049664a66ebfa61bb0fe3f04e3d09c6778a57feac8d2f6a8453bd29358f87
# Fri, 17 Nov 2023 02:18:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 17 Nov 2023 02:18:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7a1cc914f0f5e059bfdf02906a6e052b1c97cebaf91eb6c2fd835cfddebda2`  
		Last Modified: Thu, 16 Nov 2023 02:26:46 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b93b4cb5d6725beac934401f77fbf989141c12afa232cff1f25429b1a301ba73`  
		Last Modified: Thu, 16 Nov 2023 05:26:50 GMT  
		Size: 442.0 KB (441969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22088bf48f3bbce80960887fe94d86c11b50b864e902347298416ae9c621501`  
		Last Modified: Thu, 16 Nov 2023 05:26:50 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d8f6249f95be0911abdfd12a1f9bc8f3dc024f415c40647b843b72d714e2530`  
		Last Modified: Thu, 16 Nov 2023 05:26:50 GMT  
		Size: 257.3 KB (257301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25de0bfa8b996fcaf6559a07e3c27612bae15930a0da82128945f57b5fdb5c66`  
		Last Modified: Fri, 17 Nov 2023 02:21:04 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7ad978ff3404bd57ae1c76dc7fb663e18bb8de7adbcb3e46266bbb58310278`  
		Last Modified: Fri, 17 Nov 2023 02:21:04 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e711d949176d7e6e3153342552faa89e3e027b0e5d416862fcbdb1ce85b3e00`  
		Last Modified: Fri, 17 Nov 2023 02:21:04 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e3ff18b00619b613af6fefbaba8d679fcbe4e4b0c76e5b221e20cf433a479e`  
		Last Modified: Fri, 17 Nov 2023 02:21:23 GMT  
		Size: 199.2 MB (199215452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4476fb82630a83a7e85d94e755dcef8f1b717a47dfb8e2b4c53b740961991b7c`  
		Last Modified: Fri, 17 Nov 2023 02:21:04 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
