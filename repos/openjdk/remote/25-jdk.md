## `openjdk:25-jdk`

```console
$ docker pull openjdk@sha256:0c6b75490644c80c7321851c4ff5cde67af2838c220581ce8088987d29e497b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 7
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `openjdk:25-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:c6f178c727d1148b0eded6bccd0e6658d490f41be5826bc8aac0ab8ba52f6e34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.6 MB (309563136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89876c29f5fa27c233a3df61ba10a2c4b1543a3f98d66a0d1590045e8295637d`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Sat, 25 Jan 2025 01:52:19 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 25 Jan 2025 01:52:19 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 25 Jan 2025 01:52:19 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 Jan 2025 01:52:19 GMT
ENV LANG=C.UTF-8
# Sat, 25 Jan 2025 01:52:19 GMT
ENV JAVA_VERSION=25-ea+7
# Sat, 25 Jan 2025 01:52:19 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/7/GPL/openjdk-25-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='7feccd12886711c8902b12a7af32cb26a34993f148b00a36aa93068ce1e3b128'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/7/GPL/openjdk-25-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='8f29e5e012a3477812ef892a16022af8410235782f12c41d09d2a7082e20849e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 25 Jan 2025 01:52:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0ad7cd79dc68c5fb4b88ce26761b817bcac823ce273efebd361e4de5afab8c`  
		Last Modified: Tue, 28 Jan 2025 23:28:55 GMT  
		Size: 48.8 MB (48774991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df433994f66419351a00d7660295e9799688c69a1a7be99a715f8b9bfbb7cf4`  
		Last Modified: Tue, 28 Jan 2025 23:28:59 GMT  
		Size: 211.7 MB (211689443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:55113cfc0f34b69ed51ab6ac1cc314e3c1e385ae7962de4538c35bd5d423980a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4926651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d151de075a33e8a638281888a1e7fb99177d67b9b548d0b833828a4f224316fa`

```dockerfile
```

-	Layers:
	-	`sha256:d019f4df7979f6ef93de7f47df9c7940fb9a1d9a18a8913b078dcbc597ad5c59`  
		Last Modified: Tue, 28 Jan 2025 23:28:54 GMT  
		Size: 4.9 MB (4906931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:def200ddd033beceb46943a9f05e8e47fb7b2f7a301b260cace24429ee5a56e8`  
		Last Modified: Tue, 28 Jan 2025 23:28:53 GMT  
		Size: 19.7 KB (19720 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6e25057ce82fb7bdbff94cdd17261118e600af70f6953797f6d2673dc063c3ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.5 MB (306523823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a395dfb33aed0181ab531465c94c1c12231bc44f45b2fa4c9e96ea2ee122c5cd`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Sat, 25 Jan 2025 01:52:19 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 25 Jan 2025 01:52:19 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 25 Jan 2025 01:52:19 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 Jan 2025 01:52:19 GMT
ENV LANG=C.UTF-8
# Sat, 25 Jan 2025 01:52:19 GMT
ENV JAVA_VERSION=25-ea+7
# Sat, 25 Jan 2025 01:52:19 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/7/GPL/openjdk-25-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='7feccd12886711c8902b12a7af32cb26a34993f148b00a36aa93068ce1e3b128'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/7/GPL/openjdk-25-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='8f29e5e012a3477812ef892a16022af8410235782f12c41d09d2a7082e20849e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 25 Jan 2025 01:52:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9527a70a5df0c50a0919b2bbc807b6789f8d6833d49f997079d3ab5dd2e735`  
		Last Modified: Wed, 22 Jan 2025 02:29:30 GMT  
		Size: 49.2 MB (49203729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ae0949b656b700eb965121b445e19828c0619060dadef5a281201f9ec21832`  
		Last Modified: Tue, 28 Jan 2025 23:32:26 GMT  
		Size: 209.7 MB (209652702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:d838bf2bea2adc92f71afc021ddc9204fb4ed2e50fe2b3b040bacd139ccfb9d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4924701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43bf9a6c6fe3a9f6ce02a5cfb36bcccefdc69b97effffed8d6b4f7452d3bb656`

```dockerfile
```

-	Layers:
	-	`sha256:535da638224f593a367cf225f0a3b4e8d19e0b37c87f8a86b2299c4ec87c2887`  
		Last Modified: Tue, 28 Jan 2025 23:32:21 GMT  
		Size: 4.9 MB (4904693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5a8eb067d49b8f9ac78380932c6b258a3db7bdbcfb0e7271cb790402d58a94e`  
		Last Modified: Tue, 28 Jan 2025 23:32:21 GMT  
		Size: 20.0 KB (20008 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-jdk` - windows version 10.0.26100.2894; amd64

```console
$ docker pull openjdk@sha256:6b3a41a27c22d049a46022606d7fe9d04843a935866530726877fc2f792f6431
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2708840642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96b9087da181daa419a5b344df9d07bf88331b07ce95aba85c729985befe61b3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Tue, 28 Jan 2025 23:34:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 28 Jan 2025 23:34:25 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 28 Jan 2025 23:34:26 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 28 Jan 2025 23:34:31 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 28 Jan 2025 23:34:32 GMT
ENV JAVA_VERSION=25-ea+7
# Tue, 28 Jan 2025 23:34:32 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/7/GPL/openjdk-25-ea+7_windows-x64_bin.zip
# Tue, 28 Jan 2025 23:34:33 GMT
ENV JAVA_SHA256=98590eb26fdd8ac407ec4fd6fb11819d381f179d87174fea5a2ac7d5b051c11a
# Tue, 28 Jan 2025 23:34:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 28 Jan 2025 23:34:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e7940fec99849e6c960be9e26e87a2f03cc6d8e8de8234666f263fac7ddfcc`  
		Last Modified: Tue, 28 Jan 2025 23:34:57 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13bc4c27420d585013e0fde9d0b84098d044fa9ed9ed00e5881758f8b97a8687`  
		Last Modified: Tue, 28 Jan 2025 23:34:57 GMT  
		Size: 393.3 KB (393344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5870ad41af3cc4bd58210ae9b4c4d5375a4bf41f49d65642dbde8479214e95`  
		Last Modified: Tue, 28 Jan 2025 23:34:57 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6566e9d47962f37f06257e7b1d4a8e6efd54023299e0cb265fbf0d560f1948`  
		Last Modified: Tue, 28 Jan 2025 23:34:57 GMT  
		Size: 377.9 KB (377885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b354356dbf6764fab54c7f42fadd46dcab82fbdd95f1b105dffc3933032cccab`  
		Last Modified: Tue, 28 Jan 2025 23:34:55 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa635a681a20ca1df1ba7a072c3cc29f81fd54a5e577490870145e3c3b46c71f`  
		Last Modified: Tue, 28 Jan 2025 23:34:55 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1550e743196406c182237c06dde309e4cd69cf556e4f19a41edb67ced7156e17`  
		Last Modified: Tue, 28 Jan 2025 23:34:55 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb69abab699d88bc50a5b0699ccd8ef312a55e77444184ec287e0ee05740596c`  
		Last Modified: Tue, 28 Jan 2025 23:35:09 GMT  
		Size: 207.8 MB (207784025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce1f388e9621b93a739b81e37c7ab7ea549f03a98621e11c63405506d293283`  
		Last Modified: Tue, 28 Jan 2025 23:34:55 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-jdk` - windows version 10.0.20348.3091; amd64

```console
$ docker pull openjdk@sha256:609c02818812727347edc258befcbc62e1ca95c2de1c124b37c9b03f2c6f5c2a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2470803142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bbf868068a78a5f3f315a9a8dc7e1e7801463d3397b0b58b316023e6a070d08`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Tue, 28 Jan 2025 23:27:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 28 Jan 2025 23:28:54 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 28 Jan 2025 23:28:55 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 28 Jan 2025 23:29:09 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 28 Jan 2025 23:29:09 GMT
ENV JAVA_VERSION=25-ea+7
# Tue, 28 Jan 2025 23:29:10 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/7/GPL/openjdk-25-ea+7_windows-x64_bin.zip
# Tue, 28 Jan 2025 23:29:11 GMT
ENV JAVA_SHA256=98590eb26fdd8ac407ec4fd6fb11819d381f179d87174fea5a2ac7d5b051c11a
# Tue, 28 Jan 2025 23:29:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 28 Jan 2025 23:29:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1196647625f97a5c149bd4183458529ca5c7f7538c17f956c0c9fb41fc25bc40`  
		Last Modified: Tue, 28 Jan 2025 23:29:52 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d50d493298a1b0fab1293d0523955388b3b4683ded4b3551c089317141259a`  
		Last Modified: Tue, 28 Jan 2025 23:29:52 GMT  
		Size: 364.1 KB (364128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7e1212140f1b850909f77bb8249e4fc1c1b1c6b6e2b20f868a12e06ab9ecf5`  
		Last Modified: Tue, 28 Jan 2025 23:29:52 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:482262ff641b83b70fb20e68b180b1e12cd6d1e35e4a5c7c3b3ec4fbafd6b134`  
		Last Modified: Tue, 28 Jan 2025 23:29:52 GMT  
		Size: 311.9 KB (311851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d595f39aed0f24aadba29f83e2fa569812e512031bfe927cc8d2ea3ac50c469b`  
		Last Modified: Tue, 28 Jan 2025 23:29:51 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7693907405c5ef496592f9e46f3489f2dfcbb039111a1e6e8305f49fbe7c230c`  
		Last Modified: Tue, 28 Jan 2025 23:29:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9acda82acf2077e64e78db802e42fed3f40a5c39b7bb9bd851531e706a098a3e`  
		Last Modified: Tue, 28 Jan 2025 23:29:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e61106f45308b377a4ff1100526a067ef9ab3d3960f1a112e688258e2415a26`  
		Last Modified: Tue, 28 Jan 2025 23:30:02 GMT  
		Size: 207.7 MB (207734193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b815c0bd0062679933c7eb3768ed73f306cda4f2dba2455b49ca8d73f6255611`  
		Last Modified: Tue, 28 Jan 2025 23:29:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-jdk` - windows version 10.0.17763.6775; amd64

```console
$ docker pull openjdk@sha256:97edc7bcaf04450caf265fc8aa5c95bad9f5e45406b2847c88371df5372875c1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2330637094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3316370f34e0be3bee0ce03dd987f429bf893ec391497da6c360962dc17afd63`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Wed, 29 Jan 2025 00:26:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 Jan 2025 00:27:18 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 29 Jan 2025 00:27:18 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 29 Jan 2025 00:27:28 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 29 Jan 2025 00:27:29 GMT
ENV JAVA_VERSION=25-ea+7
# Wed, 29 Jan 2025 00:27:29 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/7/GPL/openjdk-25-ea+7_windows-x64_bin.zip
# Wed, 29 Jan 2025 00:27:30 GMT
ENV JAVA_SHA256=98590eb26fdd8ac407ec4fd6fb11819d381f179d87174fea5a2ac7d5b051c11a
# Wed, 29 Jan 2025 00:28:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 29 Jan 2025 00:28:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bf154cdbe7d3a6f56dd2f8dfcbd1b1e2c402968514547c80d78d40d221e931`  
		Last Modified: Wed, 29 Jan 2025 00:28:10 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777d1630c29d43e093833f18c618ad6c55bf0aa54795441fc7ce8c818e50d9ce`  
		Last Modified: Wed, 29 Jan 2025 00:28:10 GMT  
		Size: 340.2 KB (340228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155ee35ee7f973789a0d244debe9654e0a3d1eb74d1d2a4b31b2d3a4ddcd5eb6`  
		Last Modified: Wed, 29 Jan 2025 00:28:10 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c97e57488697d4457e32dc5c42280ccb954756dc0f985440cd3e3421b8a6ef`  
		Last Modified: Wed, 29 Jan 2025 00:28:10 GMT  
		Size: 330.6 KB (330638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a0e6adb71bdca75fb53fa58de058b56f06219a2a78f34c54311de8b885aaa10`  
		Last Modified: Wed, 29 Jan 2025 00:28:09 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8cd25b1c8b4c69b50897de9fe99a8cc939a835a7657576415a2c8ec9d209cc`  
		Last Modified: Wed, 29 Jan 2025 00:28:09 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e504cd2c4c9cba8e3b70b4bb1574092c66bd4c6bf3d87825909ca8bb6681dc8`  
		Last Modified: Wed, 29 Jan 2025 00:28:09 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b3ffa5deee39c2df073de8793f9455af9e200083b6dac2d89aba0395d64d14`  
		Last Modified: Wed, 29 Jan 2025 00:28:19 GMT  
		Size: 207.7 MB (207746271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ec5684877f02e1de49a3ab901983533b56eaf325d005d327280319859f532e`  
		Last Modified: Wed, 29 Jan 2025 00:28:09 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
