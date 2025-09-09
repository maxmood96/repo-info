## `openjdk:26-ea-jdk`

```console
$ docker pull openjdk@sha256:7ddd9de2224dd6440fa238107916dff732a38f8ff90a197c44401b8175d27352
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `openjdk:26-ea-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:a6775e064fb3f3f9a0214b9f4015fed719c9fca019fd2f658fd2c13c55254950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.8 MB (310791393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21cadb7b50c9a81b157e67c49f5a317027f1dc9f3fa4034f6c852af0a38e85a1`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Sat, 06 Sep 2025 00:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 06 Sep 2025 00:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 06 Sep 2025 00:48:13 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Sep 2025 00:48:13 GMT
ENV LANG=C.UTF-8
# Sat, 06 Sep 2025 00:48:13 GMT
ENV JAVA_VERSION=26-ea+14
# Sat, 06 Sep 2025 00:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/14/GPL/openjdk-26-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='14787165312e455276975549713f2f8699344989dee23e7099bafa7121b78b61'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/14/GPL/openjdk-26-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='c0b7fc80b5a73fb433db4049bb05b46ed43827c082c5bfd0b6f8883400c4d91c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Sep 2025 00:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e1b74a60e0abcb871fd5434f539541d0f3b626ce734094d202e74090106f5e`  
		Last Modified: Tue, 09 Sep 2025 00:25:05 GMT  
		Size: 38.0 MB (38007252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe8c4a2ee227258220131d1e110ee6edc891c76c1f636a0e9b17cd9cc43e1db`  
		Last Modified: Tue, 09 Sep 2025 00:26:25 GMT  
		Size: 223.3 MB (223287125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:dc496b6738b123fce0a8ba6186ae2aa9cf68000a8d78d4eeff94bbb0c1755ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3660475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2def5bd003424bb8c71b879d00a5fc8883570f198152a9818bdfb82593d3afbd`

```dockerfile
```

-	Layers:
	-	`sha256:3108e8dc0ccb84869e4df89976ae15c832697ed9d0ef25571bda594abcea995e`  
		Last Modified: Tue, 09 Sep 2025 00:24:40 GMT  
		Size: 3.6 MB (3640729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7db851c2b395008d8e485320522fea8eab318fd8abdc9d13d11290b986febae1`  
		Last Modified: Tue, 09 Sep 2025 00:24:41 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c7f2f80c56a485a936fcd2b84fc5807711ae1674bf76b7041b3b80f63ebb57c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.6 MB (307628970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa3e6241bd0182a72c7998d8c85bd40fc5ce1a425bc520bccede4af9662d8f60`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Aug 2025 17:12:13 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:12:13 GMT
CMD ["/bin/bash"]
# Sat, 06 Sep 2025 00:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 06 Sep 2025 00:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 06 Sep 2025 00:48:13 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Sep 2025 00:48:13 GMT
ENV LANG=C.UTF-8
# Sat, 06 Sep 2025 00:48:13 GMT
ENV JAVA_VERSION=26-ea+14
# Sat, 06 Sep 2025 00:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/14/GPL/openjdk-26-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='14787165312e455276975549713f2f8699344989dee23e7099bafa7121b78b61'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/14/GPL/openjdk-26-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='c0b7fc80b5a73fb433db4049bb05b46ed43827c082c5bfd0b6f8883400c4d91c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Sep 2025 00:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b5e369658cc0fdedce73e0479a85cd17ba8a09435fc3b21f6afb7e0d4783429d`  
		Last Modified: Thu, 21 Aug 2025 18:56:13 GMT  
		Size: 48.1 MB (48086723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0f06fe365088b13c3e85d9d82bb0bfa20bd800107bbd4f847969b839eee731`  
		Last Modified: Tue, 09 Sep 2025 07:54:07 GMT  
		Size: 38.4 MB (38410789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:854224966d2e4c929e49f507b0fc8eabbdc2bd4fa1be348d9e9cc3b04b851d45`  
		Last Modified: Tue, 09 Sep 2025 07:54:21 GMT  
		Size: 221.1 MB (221131458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:763a282623c2eea7f95543a02c0fefacd201813dbe9330f9f7ce3b3db99d496f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3658523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f136f09a092fbc9895c6ff8870d5f44422fc012234dc81e1e768f240dffbbd2c`

```dockerfile
```

-	Layers:
	-	`sha256:4d4726d808ef2569faecd5d3c6c000af57992a5ab4aa812fbe8d3def4b87e5b9`  
		Last Modified: Tue, 09 Sep 2025 03:24:02 GMT  
		Size: 3.6 MB (3638491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10578d2f7e704ed92514277cde235522fad1839eb62442734e389d9da3dacf19`  
		Last Modified: Tue, 09 Sep 2025 03:24:04 GMT  
		Size: 20.0 KB (20032 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk` - windows version 10.0.26100.4946; amd64

```console
$ docker pull openjdk@sha256:9e14bb2a394c7497d23a6cbf38da2f9d45600767c5d92e95165f8d264d21ed27
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3718804066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e29c9f3dcd46c6c72a6bfda7d5a1a555718c2fd8a6b410898efd2c5376263cc6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Mon, 08 Sep 2025 21:33:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 08 Sep 2025 21:33:30 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 08 Sep 2025 21:33:31 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 08 Sep 2025 21:33:37 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 08 Sep 2025 21:33:38 GMT
ENV JAVA_VERSION=26-ea+14
# Mon, 08 Sep 2025 21:33:39 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/14/GPL/openjdk-26-ea+14_windows-x64_bin.zip
# Mon, 08 Sep 2025 21:33:40 GMT
ENV JAVA_SHA256=a7542fc9e185b46aef40f54067948209eaeed10cc87b141740dc4b4236bf3d70
# Mon, 08 Sep 2025 21:33:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 08 Sep 2025 21:34:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668c2082a667bf0a02fe7b7d4f393c75215fc1dcda10d14609b2c9b912cbf42e`  
		Last Modified: Mon, 08 Sep 2025 21:57:16 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6767f1bddd3410cc38b81f8d86e4dc43ffed48f39cf72b2fdfe43e389254b8b6`  
		Last Modified: Mon, 08 Sep 2025 21:57:17 GMT  
		Size: 398.7 KB (398654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dcdc9d5ecaa544c162dc3267bc0e21961e13e4d8ecf0be1acfb65d0c46e074c`  
		Last Modified: Mon, 08 Sep 2025 21:57:18 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11abbbab1c4eec50c56da6adb68c519ec2be84955cae33f733d10b1ec0822963`  
		Last Modified: Mon, 08 Sep 2025 21:57:18 GMT  
		Size: 378.6 KB (378584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc29eae6d35b1c1ed60921038db29bc65ceeabc887618a816f3b24d0b03b8872`  
		Last Modified: Mon, 08 Sep 2025 21:57:19 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b648a8393e72737cbc693683a9b3253e2d7d22ab2b395cb0ac3dcf93e53a7623`  
		Last Modified: Mon, 08 Sep 2025 21:57:20 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b07c1bba29b7107d745eb1698157607783bf438f2bbc7ca14fd31da3668d75f`  
		Last Modified: Mon, 08 Sep 2025 21:57:21 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69bd4c9f67e487f389e86c27b9fedfc88008a4f9de98f8b4056bb66bbdc38288`  
		Last Modified: Mon, 08 Sep 2025 21:58:28 GMT  
		Size: 219.2 MB (219188569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55edb3029e84143eb0203842ceca6829aa8cc6989091dd1ed6e747c75e3e3fae`  
		Last Modified: Mon, 08 Sep 2025 21:57:29 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-ea-jdk` - windows version 10.0.20348.4052; amd64

```console
$ docker pull openjdk@sha256:2d5956b76928598b566e674b720e21f367c7cc6d5120d95c8d31632a11a6aa61
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2501577810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad9d015b4805346d928e067cde1efff0e224cc1d0dd6066e65a31a57f68c1dac`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Mon, 08 Sep 2025 21:27:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 08 Sep 2025 21:27:45 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 08 Sep 2025 21:27:46 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 08 Sep 2025 21:27:57 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 08 Sep 2025 21:27:58 GMT
ENV JAVA_VERSION=26-ea+14
# Mon, 08 Sep 2025 21:27:59 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/14/GPL/openjdk-26-ea+14_windows-x64_bin.zip
# Mon, 08 Sep 2025 21:28:01 GMT
ENV JAVA_SHA256=a7542fc9e185b46aef40f54067948209eaeed10cc87b141740dc4b4236bf3d70
# Mon, 08 Sep 2025 21:28:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 08 Sep 2025 21:28:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da8b7f00b02ef88e50b9b6ff2d8aac6ce398cf1b688a04fccb942072ec3cc03`  
		Last Modified: Mon, 08 Sep 2025 21:33:18 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0bdc62258e02f28ebb4d3628071116d485f0de02f5161fff9ea7321161dd59`  
		Last Modified: Mon, 08 Sep 2025 21:33:20 GMT  
		Size: 360.7 KB (360691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942661a805b183d1ce376ad91885e832c3ebdad6cd13b63e7d1dad9f6cf79950`  
		Last Modified: Mon, 08 Sep 2025 21:33:21 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f7d30277552ff9628efb52bedb2a6c95c87000b80065ad77e68b687142643d`  
		Last Modified: Mon, 08 Sep 2025 21:33:23 GMT  
		Size: 346.9 KB (346943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7df437b6b3fb573b600ca81a78d4f9a8d09f9c50ef7f6dc073a337204362c6`  
		Last Modified: Mon, 08 Sep 2025 21:33:27 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e8d61b25da266bf702ac880e29445231b5ae8e436b0e6307a75e0f5357915e`  
		Last Modified: Mon, 08 Sep 2025 21:33:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37cfe8e4023908369a77043604ac4dc35e10e7496c4b5a8d9045ca4b59b86bb9`  
		Last Modified: Mon, 08 Sep 2025 21:33:30 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b02170a8ac4bb2383c8976d86514b8e3d091fac8024fad26010424f9e65fea`  
		Last Modified: Mon, 08 Sep 2025 21:35:09 GMT  
		Size: 219.2 MB (219170485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:960e467af9e508f8d778009e0104a990df7faece67dd89179c930ce087a69bbb`  
		Last Modified: Mon, 08 Sep 2025 21:33:31 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
