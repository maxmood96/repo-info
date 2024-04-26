## `openjdk:23-ea-jdk`

```console
$ docker pull openjdk@sha256:82ae9011c5908852930cfd9fafa63a99df8437eb137242a2f5b22d4c233bba65
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

### `openjdk:23-ea-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:b8f01156f9b7b63addb2257d3e564e2c963f8c9f7a16dd238b161781251583e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.5 MB (297546474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73913e3a78874b1fdfe8fe2517e2f4a7014202023821363bf244f5b90cd69069`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 12 Apr 2024 18:48:10 GMT
ADD file:6a8fca96158e62daae8905c2aa3ae7ac8614dfb3918aa6baed38c15923bfb4e6 in / 
# Fri, 12 Apr 2024 18:48:10 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 18:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 12 Apr 2024 18:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 12 Apr 2024 18:48:10 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 18:48:10 GMT
ENV LANG=C.UTF-8
# Fri, 12 Apr 2024 18:48:10 GMT
ENV JAVA_VERSION=23-ea+18
# Fri, 12 Apr 2024 18:48:10 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/18/GPL/openjdk-23-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='618c320c28c4d2d71fd5a366876b5f9ef8cf16819e9793e7d960ecea1caf9d5d'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/18/GPL/openjdk-23-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='aecde065716b2226217e12905a714da37b06daca526e77821a55d09eab1b5489'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Apr 2024 18:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0f6737e7f9187a51747790f2636510ac11e4d7718c4a8927053f6ec486848303`  
		Last Modified: Thu, 25 Apr 2024 01:43:54 GMT  
		Size: 49.0 MB (48965144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c42c936f6a49ca30c0c679e7d5a2c22a2840f747b55d1d5b95831b4d948220b`  
		Last Modified: Thu, 25 Apr 2024 02:55:39 GMT  
		Size: 37.7 MB (37728436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfbda0f11910b55dad8f538a3371f98acc7fa3ba6d81f2bd8818876afb6ebd5`  
		Last Modified: Thu, 25 Apr 2024 02:55:41 GMT  
		Size: 210.9 MB (210852894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:88b87f1c2b9cda5bcfd85f9e7ff8a11e40f2c4ab86392c815025b074177e8063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3349454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee486e8b79c0e75a5da635210fe5b449f90c2fc901e3e406bb08338a25fbfd7`

```dockerfile
```

-	Layers:
	-	`sha256:b2ab1b36a0a10396ba9b146f036537657810b99b68badf72ff67795595b8435d`  
		Last Modified: Thu, 25 Apr 2024 02:55:38 GMT  
		Size: 3.3 MB (3329561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd8028353c594881dc923a03ac82a064d202794f44116d4ec2d05f33e6c54d3c`  
		Last Modified: Thu, 25 Apr 2024 02:55:38 GMT  
		Size: 19.9 KB (19893 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:54b2b3461c161cd6ca9d852e536206526f2c2fff1bc9dd36704d98d1b4c9f446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294540512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:669d197c22957cb711f6a89f3d0446dbb44f5001d3b4046ea8f473f0f9090dfe`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 12 Apr 2024 18:48:10 GMT
ADD file:25023c55a282c7a0be958dc9555d115ad07185cff37f25566562575bc91f2d6e in / 
# Fri, 12 Apr 2024 18:48:10 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 18:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 12 Apr 2024 18:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 12 Apr 2024 18:48:10 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 18:48:10 GMT
ENV LANG=C.UTF-8
# Fri, 12 Apr 2024 18:48:10 GMT
ENV JAVA_VERSION=23-ea+18
# Fri, 12 Apr 2024 18:48:10 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/18/GPL/openjdk-23-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='618c320c28c4d2d71fd5a366876b5f9ef8cf16819e9793e7d960ecea1caf9d5d'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/18/GPL/openjdk-23-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='aecde065716b2226217e12905a714da37b06daca526e77821a55d09eab1b5489'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Apr 2024 18:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6c095c52d5d232eeebfdc7173cf1b5de6af5dfcf6cc906a66496ba14cf0ffcee`  
		Last Modified: Wed, 24 Apr 2024 23:30:37 GMT  
		Size: 47.7 MB (47662476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5998d81da777dd4f81d01a63cd4676cc2bd3824fbd23c02af639d3bfbc80f43`  
		Last Modified: Fri, 26 Apr 2024 08:23:15 GMT  
		Size: 38.1 MB (38142556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b7bef8bbbf8792d8ce4e69762522349aaae4a93772bff6592527432031abed`  
		Last Modified: Fri, 26 Apr 2024 08:23:18 GMT  
		Size: 208.7 MB (208735480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:4a9364b3163a521968db1aaf8375392e1c04063ea0491fe24a353000c705c982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3347689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ffc53a75a1c1b6e200bbc511aa7ab872b6a756f5cfe8a6d010252a8e9ae40b7`

```dockerfile
```

-	Layers:
	-	`sha256:af3e25353f706d984af4fbaf8581d734efa78d2349903ea2b3abad80be392f53`  
		Last Modified: Fri, 26 Apr 2024 08:23:14 GMT  
		Size: 3.3 MB (3327759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5d8032e7dcc48e0ea779943dd24d20306437d20d9bdb91ca793b8430c8caf8d`  
		Last Modified: Fri, 26 Apr 2024 08:23:14 GMT  
		Size: 19.9 KB (19930 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-jdk` - windows version 10.0.20348.2402; amd64

```console
$ docker pull openjdk@sha256:ed699f6c194cf914242c906abf8a605cbeca8c3edfc9880c9cb6f60df4001605
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2205921058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb836d326b1123622cf58600381e176641b5d1188ba33aacbbe6329de63bd28`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Mon, 15 Apr 2024 18:01:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 15 Apr 2024 18:02:19 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 15 Apr 2024 18:02:20 GMT
ENV JAVA_HOME=C:\openjdk-23
# Mon, 15 Apr 2024 18:02:26 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 15 Apr 2024 18:02:27 GMT
ENV JAVA_VERSION=23-ea+18
# Mon, 15 Apr 2024 18:02:27 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/18/GPL/openjdk-23-ea+18_windows-x64_bin.zip
# Mon, 15 Apr 2024 18:02:28 GMT
ENV JAVA_SHA256=b6d83c7e42b15f6a6d0bcbd83496ba05df366fceaa6bd6314550fd8b7eb9c19d
# Mon, 15 Apr 2024 18:02:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 15 Apr 2024 18:02:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5deba58106036304abd3657ddb9beebdf9c2ec2dc8941c08ceab69865956ca9b`  
		Last Modified: Mon, 15 Apr 2024 18:02:55 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa83e06c3826ffac84056aeaedb4230c8925ef0e298281609e1107fb54dfd18a`  
		Last Modified: Mon, 15 Apr 2024 18:02:55 GMT  
		Size: 502.9 KB (502894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32c7053139a8a4450f84a488bdc42fe24c4a155b83d932c583ea062fa9f85e3`  
		Last Modified: Mon, 15 Apr 2024 18:02:54 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0adaa43b7de34c3504216b987e7bafc40e1f14150d15a344c5d07685463afea`  
		Last Modified: Mon, 15 Apr 2024 18:02:54 GMT  
		Size: 353.3 KB (353280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e62f4e5fa3cd111da0818a8d6be16f458e1fc5e162065521f1d9135a8fec266e`  
		Last Modified: Mon, 15 Apr 2024 18:02:53 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc2450d2e190a0c9c440071a7f51890a8963787114863522701ad3609287992`  
		Last Modified: Mon, 15 Apr 2024 18:02:53 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5087a5b39fafa5bbb42267d0f4f04cd66bd3d57f9ad2f9ecd0900737b123a6ca`  
		Last Modified: Mon, 15 Apr 2024 18:02:53 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366404b41357e69347111c57454ee95845df92995d879aaf887a968d87ab5c96`  
		Last Modified: Mon, 15 Apr 2024 18:03:05 GMT  
		Size: 205.7 MB (205683505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:273ba895224593049b1baa8aa148113d5d8d2a7c793415e825a6904d14858977`  
		Last Modified: Mon, 15 Apr 2024 18:02:53 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:23-ea-jdk` - windows version 10.0.17763.5696; amd64

```console
$ docker pull openjdk@sha256:04dc47e029b9be3af615d4eb1cccfa4b2046901e3b1612d49054bd9ce00439ce
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2370908385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d8a3fd5bdf631b3902fcdbd08594f0d3176234f0ac33494aa5c21fc71c6a14b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Mon, 15 Apr 2024 17:55:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 15 Apr 2024 17:56:23 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 15 Apr 2024 17:56:23 GMT
ENV JAVA_HOME=C:\openjdk-23
# Mon, 15 Apr 2024 17:56:44 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 15 Apr 2024 17:56:45 GMT
ENV JAVA_VERSION=23-ea+18
# Mon, 15 Apr 2024 17:56:45 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/18/GPL/openjdk-23-ea+18_windows-x64_bin.zip
# Mon, 15 Apr 2024 17:56:46 GMT
ENV JAVA_SHA256=b6d83c7e42b15f6a6d0bcbd83496ba05df366fceaa6bd6314550fd8b7eb9c19d
# Mon, 15 Apr 2024 17:57:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 15 Apr 2024 17:57:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d57ee42b907f79467ecca73f3d0c450501cd94133ab84f8dd9ed9c39d118fed`  
		Last Modified: Mon, 15 Apr 2024 17:57:32 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:569330eec2432fb352536dbc02e2239d5479b3fed23a1c742f146de1a9b38691`  
		Last Modified: Mon, 15 Apr 2024 17:57:32 GMT  
		Size: 459.0 KB (459020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe35775d6b9206371ed754089db9aab8bb43d12cb14de7992d622c1382e6394`  
		Last Modified: Mon, 15 Apr 2024 17:57:32 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f108a3e0bef9d119d47f4141108b9137388c5f204683a3a524fc60fa3be241d0`  
		Last Modified: Mon, 15 Apr 2024 17:57:32 GMT  
		Size: 334.3 KB (334348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace323dc01cc31b8da2542bf69b62f201a73f79501b87c4707fb0f498e622b43`  
		Last Modified: Mon, 15 Apr 2024 17:57:30 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbba8befdf04fc0a2517f50d9240569990ab2d956292b7406c95cc08669c58b0`  
		Last Modified: Mon, 15 Apr 2024 17:57:30 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3580f0fe8488469c1155438702ce661d3d8e092499059a3090fc684c600db5`  
		Last Modified: Mon, 15 Apr 2024 17:57:30 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02fc119f88b3c8275608ff8e9de2d960ccba14f02bdcc5a91fefa135e43ef826`  
		Last Modified: Mon, 15 Apr 2024 17:57:42 GMT  
		Size: 205.7 MB (205679260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d54a85f11777c34ffb8a3f28fa8d0d5d83c45262ccd2ee2aca9a08c16e39d769`  
		Last Modified: Mon, 15 Apr 2024 17:57:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
