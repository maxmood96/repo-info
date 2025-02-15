## `openjdk:24-jdk`

```console
$ docker pull openjdk@sha256:959b0bbd4c449b96b5031b859e1b3e140bc421dab65374556502e429666779d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 7
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `openjdk:24-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:c523c191d7e471170f6a4184da41f07b579869f531865823e931c43f7c1db1fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.7 MB (310696539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deea31ac117607ba80134d346eb1dc2f0d8b4ab32eb292d8ed6591fd5154da0c`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Feb 2025 01:48:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
CMD ["/bin/bash"]
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 07 Feb 2025 01:48:12 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Feb 2025 01:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_VERSION=24
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-x64_bin.tar.gz'; 			downloadSha256='88b090fa80c6c1d084ec9a755233967458788e2c0777ae2e172230c5c692d7ef'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-aarch64_bin.tar.gz'; 			downloadSha256='a03867ed061c7bb661231e62b0967ff5a5a0b1bbaa37bdead3a924bd2ba3215f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:43759093d4f6232b149ce0851c768f0287c95e1e0e34de29dac7c632ed93cc86`  
		Last Modified: Sat, 15 Feb 2025 00:31:02 GMT  
		Size: 49.1 MB (49090891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd758b5cdc0820cd282118aa6035c71428802b729afa056fccb151397acccf0a`  
		Last Modified: Sat, 15 Feb 2025 02:10:02 GMT  
		Size: 48.8 MB (48768601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d04b07e7673fe63f27989699cac217c32fca630b277edca3b6b2e6a9186373`  
		Last Modified: Sat, 15 Feb 2025 02:10:06 GMT  
		Size: 212.8 MB (212837047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:73346847fd2bb9a7b8f07f733b2a3d03f9cfb9be048cfc1bb3c2bb567ce73fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4927337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7564c366311efb7099bb044c07cfc7977fb68702d0ba2cf04c527a34f93e7208`

```dockerfile
```

-	Layers:
	-	`sha256:d4a2100e9eb7b770519cfde2d824374c6061ab932bca9c5d7c1f81a23071f5cd`  
		Last Modified: Sat, 15 Feb 2025 01:23:16 GMT  
		Size: 4.9 MB (4909455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3eda9eb3385d5fa1b05c68bc5d519801cdcfff2f99dd428c3fc59977266e7e06`  
		Last Modified: Sat, 15 Feb 2025 01:23:16 GMT  
		Size: 17.9 KB (17882 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:47a960decf116da8bac771d2e04c85835fc8872e4b01d8fc083f16e7e4032af8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.6 MB (307645021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b7b045d4d2bfa4b54ebd1d8e9c4ab4a249522e726eae949f138a79c9245772a`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Feb 2025 01:48:12 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
CMD ["/bin/bash"]
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 07 Feb 2025 01:48:12 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Feb 2025 01:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_VERSION=24
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-x64_bin.tar.gz'; 			downloadSha256='88b090fa80c6c1d084ec9a755233967458788e2c0777ae2e172230c5c692d7ef'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-aarch64_bin.tar.gz'; 			downloadSha256='a03867ed061c7bb661231e62b0967ff5a5a0b1bbaa37bdead3a924bd2ba3215f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:903087d703a78a4fd0935e14d3e7b29819d5f670ff2ee18f1691359f349f34ba`  
		Last Modified: Sat, 15 Feb 2025 07:11:23 GMT  
		Size: 47.7 MB (47669215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca163d5e019bf3d8fffa833ce86f630b0f296399ec45fe5da979a5e604b2e20`  
		Last Modified: Sat, 15 Feb 2025 13:36:07 GMT  
		Size: 49.2 MB (49187884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aac2acf1aef584af944f1f1193da211778df744f6616cfaa8a1ac094ac65b1a0`  
		Last Modified: Sat, 15 Feb 2025 14:43:26 GMT  
		Size: 210.8 MB (210787922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:b3d706d4ba2548dfef5fb14dcad2a5caac4b4e935850c18608ff10f628194f2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4925242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888a504c83af21708e3117c7d2d2e31faeb1a27f2d035ac5da9de3fd610447e1`

```dockerfile
```

-	Layers:
	-	`sha256:7ebf9352bb9ea5e912f3544068d35e75d720e7639aad456febe11ba294a277a3`  
		Last Modified: Sat, 15 Feb 2025 13:23:18 GMT  
		Size: 4.9 MB (4907145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a84664090ba131788a1a4b054b8379c23387e1e472319098c6e6b212ef7a665`  
		Last Modified: Sat, 15 Feb 2025 13:23:19 GMT  
		Size: 18.1 KB (18097 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk` - windows version 10.0.26100.2894; amd64

```console
$ docker pull openjdk@sha256:04ebeba240aa22d687e4a2b719f67346d103f87ab2f91acd4f6289ac88fd5142
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2709986938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590aea82123aa8e9e2749528909cb9240db53a967c6595bb6d3931fb1c53cff9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Tue, 11 Feb 2025 00:31:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Feb 2025 00:31:18 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 11 Feb 2025 00:31:19 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 11 Feb 2025 00:31:25 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 11 Feb 2025 00:31:25 GMT
ENV JAVA_VERSION=24
# Tue, 11 Feb 2025 00:31:26 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_windows-x64_bin.zip
# Tue, 11 Feb 2025 00:31:27 GMT
ENV JAVA_SHA256=11d1d9f6ac272d5361c8a0bef01894364081c7fb1a6914c2ad2fc312ae83d63b
# Tue, 11 Feb 2025 00:32:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 11 Feb 2025 00:32:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Wed, 22 Jan 2025 06:04:03 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d7dcf2bcddbdad7557da19e4234025bb6a672cf3b88d03d0878b8727c1bce8`  
		Last Modified: Wed, 12 Feb 2025 00:09:42 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c89eca89aa9b4ff4cfaa8458d6aee96174fd7c425a419c78542549083b507b`  
		Last Modified: Wed, 12 Feb 2025 21:53:58 GMT  
		Size: 385.6 KB (385592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ec3d96e893ae4cf1140e0c0ae61870b8f8c519be0eb742121d270436321f75`  
		Last Modified: Wed, 12 Feb 2025 00:10:22 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:400d617e06805df508fa1d5d31e2d49009c61e98ff9346d6f5d376659579e92d`  
		Last Modified: Wed, 12 Feb 2025 21:54:00 GMT  
		Size: 374.4 KB (374419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7a5cc4ea843ab82cfaf65322b1e954c32866d55945930f43bda5ab255817f2`  
		Last Modified: Wed, 12 Feb 2025 21:54:01 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca19dc597d5c6c429a93c8942fb9e69e24a066b6fbc0a4d672479547439db5f9`  
		Last Modified: Wed, 12 Feb 2025 21:54:02 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33d36d047931df06992b594d27cc88cc0155a495db3dcca47df8e43daab8c01d`  
		Last Modified: Wed, 12 Feb 2025 21:54:03 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32fc012a3383812a106bee99c2a72766783a951c214f3f919f8bb542dec6b73a`  
		Last Modified: Wed, 12 Feb 2025 21:54:19 GMT  
		Size: 208.9 MB (208941499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081f56f2a7db3acf106d80ad462a353e2ec78a9010bea88735231d862eaf05bb`  
		Last Modified: Wed, 12 Feb 2025 21:54:21 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-jdk` - windows version 10.0.20348.3207; amd64

```console
$ docker pull openjdk@sha256:dbd310fa8c9a143457931c62f1227b78dc0af70541b0edc78ea2b2f81018a4fe
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2473452909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147ddccb4f3a1c1b52b3ab70f5e4775c85f6098aa5b05241050e067e337b4811`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:44:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:44:28 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:44:29 GMT
ENV JAVA_HOME=C:\openjdk-24
# Thu, 13 Feb 2025 00:44:34 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:44:35 GMT
ENV JAVA_VERSION=24
# Thu, 13 Feb 2025 00:44:36 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_windows-x64_bin.zip
# Thu, 13 Feb 2025 00:44:36 GMT
ENV JAVA_SHA256=11d1d9f6ac272d5361c8a0bef01894364081c7fb1a6914c2ad2fc312ae83d63b
# Thu, 13 Feb 2025 00:44:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:45:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Wed, 12 Feb 2025 22:14:21 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f8491ac0764676a31a9ca542f28ff77d33c41360022d12faa4146d4ec83800`  
		Last Modified: Thu, 13 Feb 2025 01:08:58 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b3b2ffc0778175ac2bbef45d92d94d755bbed684fadf9778fcc4b0b60b95b6`  
		Last Modified: Thu, 13 Feb 2025 01:08:58 GMT  
		Size: 357.5 KB (357504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75299c43cce9196f5ad623666999a2aeab7946ea525f72e8f300feda4f7f1495`  
		Last Modified: Thu, 13 Feb 2025 01:08:59 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:615c5797bac28589910968fec6b38467ee1324b6642ca03a220836cf2d8e2e7b`  
		Last Modified: Thu, 13 Feb 2025 01:08:59 GMT  
		Size: 336.8 KB (336800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56a7abb6139aacf6df2ed9489a26de81a281a8318d145be3425038c1e14a6bb`  
		Last Modified: Thu, 13 Feb 2025 01:09:00 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0be84dc123e3d8b4c2de0ac29abc501fb897cf34ddc30f47572f0a0811a0b0`  
		Last Modified: Thu, 13 Feb 2025 01:09:00 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0676af04befdf7c26d7ee49c119d8b753b095dc84c9b6a3f4a76896db07c5926`  
		Last Modified: Thu, 13 Feb 2025 01:09:00 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e77a8548b3c12fafcb6bf10d2fc36f67d766274da0519712ef123a3de59b8ccb`  
		Last Modified: Thu, 13 Feb 2025 01:09:15 GMT  
		Size: 208.9 MB (208892900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01bfb8a1317016ff6d127a3f02ac68af478c7bd5b5c12251a7cfa96dbcadf8f`  
		Last Modified: Thu, 13 Feb 2025 01:09:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-jdk` - windows version 10.0.17763.6893; amd64

```console
$ docker pull openjdk@sha256:25694d35528c91fe01db3499f91965f40ca8110f4043a4c3633f14d60b87d642
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346492020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e6438cd1157e60ba3c39de1e3357fbbd1f5e739a6e6bcd131f4552f2fed4299`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:42:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:43:04 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:43:04 GMT
ENV JAVA_HOME=C:\openjdk-24
# Thu, 13 Feb 2025 00:43:10 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:43:11 GMT
ENV JAVA_VERSION=24
# Thu, 13 Feb 2025 00:43:11 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_windows-x64_bin.zip
# Thu, 13 Feb 2025 00:43:12 GMT
ENV JAVA_SHA256=11d1d9f6ac272d5361c8a0bef01894364081c7fb1a6914c2ad2fc312ae83d63b
# Thu, 13 Feb 2025 00:43:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:43:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 22:29:28 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59e7cb2f62d3ca1d2757aa07b43050cdda0aace6c3a7c146447f56f7dbb6be8`  
		Last Modified: Thu, 13 Feb 2025 01:08:52 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e2d27469f40aab79d4d3299885df66666ef0813aa9ea0c6787d01a97e0156d5`  
		Last Modified: Thu, 13 Feb 2025 01:08:52 GMT  
		Size: 346.9 KB (346929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc25ade87dd2f091d7f34c0fa9d5748173d7608deb415ef2f42a42ac6854447`  
		Last Modified: Thu, 13 Feb 2025 01:08:52 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76707d48dffe35b117a39312702b0279c644514e400b67f3841559be4c7285c`  
		Last Modified: Thu, 13 Feb 2025 01:08:53 GMT  
		Size: 329.3 KB (329327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b17ec1bc8b5892e08af7aa89a01850c3722831bac79e83fe575249c7b0db89`  
		Last Modified: Thu, 13 Feb 2025 01:08:53 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02abd5f6b0dc6b84975c71385c18c52ec05e69637cb94e4ec6293dcad6feb656`  
		Last Modified: Thu, 13 Feb 2025 01:08:53 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779683b99488fec228227d490079317a08e9bfef0b530951098328169b92ccc4`  
		Last Modified: Thu, 13 Feb 2025 01:08:54 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b995b9ee44c3800b99be70b7716b82aa91383a3bf22309af3e10d56f239e7e43`  
		Last Modified: Thu, 13 Feb 2025 01:09:11 GMT  
		Size: 208.9 MB (208899229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe70d0375ff31f8ef2f5a4d206a15549b5cbb1bce97545fc3d46b8f0c6981d6`  
		Last Modified: Thu, 13 Feb 2025 01:08:55 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
