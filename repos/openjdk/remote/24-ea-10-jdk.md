## `openjdk:24-ea-10-jdk`

```console
$ docker pull openjdk@sha256:181560817b7955d2658ce7f0fba10cf73076116b9d66089263ea6854d07c2cd8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.20348.2655; amd64
	-	windows version 10.0.17763.6189; amd64

### `openjdk:24-ea-10-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:7a5a1d2afa3a9a94b07c0f8dd674cca6a5d71248bdcec1f44449cbc8423831fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.8 MB (299792375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd2be6ae4495d46d1bf9a037e6235a6e60c399fe6272293bc565ce8f2019ba7`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
CMD ["/bin/bash"]
# Sat, 10 Aug 2024 00:48:15 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 10 Aug 2024 00:48:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Sat, 10 Aug 2024 00:48:15 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Aug 2024 00:48:15 GMT
ENV LANG=C.UTF-8
# Sat, 10 Aug 2024 00:48:15 GMT
ENV JAVA_VERSION=24-ea+10
# Sat, 10 Aug 2024 00:48:15 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/10/GPL/openjdk-24-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='b4c878f685a1333de0743bc33fb94a6cbd60e1ddda7e1d88068c2acc1c91012b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/10/GPL/openjdk-24-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='3640a7ecb431e631d5d23e96d0df679fb45cfed38f527a3810caeebebc44a3a5'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 10 Aug 2024 00:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf79bae0630d45787fedb5fa953cc436dfc12274f55a4f452528c4b1ef7ab5e0`  
		Last Modified: Mon, 12 Aug 2024 17:59:25 GMT  
		Size: 39.0 MB (39047374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3725799aed99a347a32658dba672a4a23ef876e1e847c9ff71fc13c12a0851ef`  
		Last Modified: Mon, 12 Aug 2024 17:59:29 GMT  
		Size: 211.8 MB (211751265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-10-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:5f0d76ab4ccef6b262be79532509dcc5960501f3159aaa0eeabb82c60867ea94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3565505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4812f20e22dde0716831844048072798e46204267203326d81985ec3479e0bf0`

```dockerfile
```

-	Layers:
	-	`sha256:f6f4bddd91a09398ed5f92fe019a04b7206d988bd8ceb92761e6e11a7fce1195`  
		Last Modified: Mon, 12 Aug 2024 17:59:24 GMT  
		Size: 3.5 MB (3545977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:613d14a3d1edb71f7edff845d1a45a52f7da3fcd4984325f2ba72f6ea1cab775`  
		Last Modified: Mon, 12 Aug 2024 17:59:24 GMT  
		Size: 19.5 KB (19528 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-10-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c15c998838b3edb32de918bf31ac7f0da26c476a9a1cd02fbaf2602c23b7d995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.7 MB (296732116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59dddc7a8d94ca4ecb80da85b22b98ca653e1ed4bbfa6d40de870a60b674a598`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Jul 2024 22:40:25 GMT
ADD file:a5d614a69430ac76660689e833533429bd70568280b25af98af60b01a76d6139 in / 
# Mon, 08 Jul 2024 22:40:26 GMT
CMD ["/bin/bash"]
# Sat, 10 Aug 2024 00:48:15 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 10 Aug 2024 00:48:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Sat, 10 Aug 2024 00:48:15 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Aug 2024 00:48:15 GMT
ENV LANG=C.UTF-8
# Sat, 10 Aug 2024 00:48:15 GMT
ENV JAVA_VERSION=24-ea+10
# Sat, 10 Aug 2024 00:48:15 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/10/GPL/openjdk-24-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='b4c878f685a1333de0743bc33fb94a6cbd60e1ddda7e1d88068c2acc1c91012b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/10/GPL/openjdk-24-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='3640a7ecb431e631d5d23e96d0df679fb45cfed38f527a3810caeebebc44a3a5'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 10 Aug 2024 00:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c72f53f7235bf26fdb27eaeb0d712fc1886f19eda2722ef9709dda7424814b9e`  
		Last Modified: Mon, 08 Jul 2024 22:41:23 GMT  
		Size: 47.7 MB (47652661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e12335bb1126bd80cd31b34b4fde93f2ccb7bb979403e778624cb60c3ece28c`  
		Last Modified: Mon, 29 Jul 2024 16:56:31 GMT  
		Size: 39.5 MB (39479870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a0a3983fbeb53dc3831ff1c0b6de018a7d416830f60d292b33cb0d580f0e37`  
		Last Modified: Mon, 12 Aug 2024 18:29:06 GMT  
		Size: 209.6 MB (209599585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-10-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:89ba66d189308793ed7fed583c49db2305794310ccbb07a55e6a073f251583ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3564362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd5e8882b9edb11850dc3777dc43ab2fce961afca9bcd0a7db0e4a29980e132b`

```dockerfile
```

-	Layers:
	-	`sha256:c32c7ce1e8379d45944da4f095d1ba1982ec6bf5492c00d5c55413034d33080d`  
		Last Modified: Mon, 12 Aug 2024 18:29:02 GMT  
		Size: 3.5 MB (3544360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba08e1d1442cdffbe04bfb5bc5d76f96b8a340f7521b75b361c2f4bd2ecf5172`  
		Last Modified: Mon, 12 Aug 2024 18:29:02 GMT  
		Size: 20.0 KB (20002 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-10-jdk` - windows version 10.0.20348.2655; amd64

```console
$ docker pull openjdk@sha256:d52eeeabd973b567feecf9e800b3649b0d118caf4111aff1e0c02e3ecab0f2c7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2349417918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b522e6bc9fb2152a8c89473a01ccfe7c6daa571ae1d11eb78d33f4058fb434c5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Tue, 13 Aug 2024 20:13:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Aug 2024 20:13:34 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 13 Aug 2024 20:13:35 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 13 Aug 2024 20:13:41 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 13 Aug 2024 20:13:41 GMT
ENV JAVA_VERSION=24-ea+10
# Tue, 13 Aug 2024 20:13:42 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/10/GPL/openjdk-24-ea+10_windows-x64_bin.zip
# Tue, 13 Aug 2024 20:13:43 GMT
ENV JAVA_SHA256=a4e5b50291add1d88baf1093f1a4822dc3ee939111b1e039214cd2fcd729dc27
# Tue, 13 Aug 2024 20:14:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 13 Aug 2024 20:14:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ab28e95f09f19e842c6141f85f4141146d831501271eeb1e181d28a1741143b`  
		Last Modified: Tue, 13 Aug 2024 20:14:08 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3cd8ffae97152c15155cf0992e6663d4d3a0a84799ea075e800d4862798d07`  
		Last Modified: Tue, 13 Aug 2024 20:14:09 GMT  
		Size: 370.9 KB (370933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96af40df3201c4d5565c5903f470cc51d0c8eff6a1992b5e2f77b734610a02e2`  
		Last Modified: Tue, 13 Aug 2024 20:14:08 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9cdce7bf58f142c2059f9559f212a75a82c04ea7b7a679de1ce35e938eae54`  
		Last Modified: Tue, 13 Aug 2024 20:14:09 GMT  
		Size: 352.7 KB (352714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:513e57d2a28c8c90f37a28361fae704e8bc9b80338f09303625047dc791cc6e4`  
		Last Modified: Tue, 13 Aug 2024 20:14:06 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7859c033fc5d4b14a43b34069650b332d1679a000cba9da15dba473dd3b106`  
		Last Modified: Tue, 13 Aug 2024 20:14:06 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d3a3244ade847b16c01fc629d75708c70ceafc8f290e9f0edca09945b2314ff`  
		Last Modified: Tue, 13 Aug 2024 20:14:06 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20bc37b909a718916d270122c4f470f53ca08a48a02669f72054b5a9ace12dae`  
		Last Modified: Tue, 13 Aug 2024 20:14:17 GMT  
		Size: 206.9 MB (206921595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ecbd2cfb18f673437c2e414f6b176dd41f0c4270455e5f2212241cc43dd307`  
		Last Modified: Tue, 13 Aug 2024 20:14:07 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-ea-10-jdk` - windows version 10.0.17763.6189; amd64

```console
$ docker pull openjdk@sha256:b37a707c3a6c0cf670aa51a58757988f48344785042a968991db413781ecd859
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2452970727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0de14bf0f97d22d36db3ad47da5fa1bfdd77b4bf71630ff180abf12fedc3e3d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Tue, 13 Aug 2024 20:19:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Aug 2024 20:20:23 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 13 Aug 2024 20:20:23 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 13 Aug 2024 20:20:40 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 13 Aug 2024 20:20:41 GMT
ENV JAVA_VERSION=24-ea+10
# Tue, 13 Aug 2024 20:20:41 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/10/GPL/openjdk-24-ea+10_windows-x64_bin.zip
# Tue, 13 Aug 2024 20:20:41 GMT
ENV JAVA_SHA256=a4e5b50291add1d88baf1093f1a4822dc3ee939111b1e039214cd2fcd729dc27
# Tue, 13 Aug 2024 20:21:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 13 Aug 2024 20:21:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19bbc6a3aa98c991beb51d75c3b0738eeb4fe060ae94448aa6e66a570d9ced86`  
		Last Modified: Tue, 13 Aug 2024 20:21:20 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a497c9508b4b83debe0298bdf5e425c0f5023a475045ac6787a533cdad9fc3d`  
		Last Modified: Tue, 13 Aug 2024 20:21:20 GMT  
		Size: 492.0 KB (492004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ed5838d7ab36f025c6d3fad97291e181a9fcc588be25ee8f94459a68508d34`  
		Last Modified: Tue, 13 Aug 2024 20:21:20 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89efff1f8dde9819449f91230d92702e4d75bc71c6577d0e571d4d1197ded16`  
		Last Modified: Tue, 13 Aug 2024 20:21:20 GMT  
		Size: 339.1 KB (339101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a22b772fa78396e7af8ed9842da3d87496b6b424c22e6bbd7bb31ff170538b7`  
		Last Modified: Tue, 13 Aug 2024 20:21:19 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad8b1368970f0ff7b2449a6d9cfdcc75139ecf30377cd2f9968492bd31b2d9a`  
		Last Modified: Tue, 13 Aug 2024 20:21:19 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff08f9d2ab02fe49a596aca68a3ddbedd40504d1247d9bb44c01b94c3ae20bb`  
		Last Modified: Tue, 13 Aug 2024 20:21:19 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7a2cf64d23941c627096e36287d3b6c289935d808dd5e999a97e5240387c05`  
		Last Modified: Tue, 13 Aug 2024 20:21:30 GMT  
		Size: 206.9 MB (206928563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a67019946cf2c72aa747350fa34b6eafdb20ee685626e48d76387df2d5b9ec4e`  
		Last Modified: Tue, 13 Aug 2024 20:21:19 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
