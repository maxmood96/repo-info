## `openjdk:27-ea-24-jdk`

```console
$ docker pull openjdk@sha256:31bde06b6f4c17a103315ffcf7179d0d0cc64d18bb90526f54de3c4762811009
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `openjdk:27-ea-24-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:19fc1624a9bf10152440f71173af202a30878eafd52f7e5cfc0d865867fcbd68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.6 MB (307648803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62012a908cb20d64322470def7cade793aa637fb6f70046301c47d2313aaa7eb`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:44:08 GMT
ADD oraclelinux-10-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:08 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 07:11:36 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 02 Jun 2026 07:11:44 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 02 Jun 2026 07:11:44 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 07:11:44 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 07:11:44 GMT
ENV JAVA_VERSION=27-ea+24
# Tue, 02 Jun 2026 07:11:44 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/24/GPL/openjdk-27-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='eb8d0fac160a096fc406b794465b245a8b40cb1b04bbb4c5824393cde263a8b5'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/24/GPL/openjdk-27-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='832ef5a271052b9065f2b5b7a63ecdbbd0363edd74228736bab7227b45b21a66'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 02 Jun 2026 07:11:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ded2aa0abafd1e1e93e05338cb1b14916dbeb283d3862aa21e5d8b0164f4cbf3`  
		Last Modified: Tue, 12 May 2026 18:44:20 GMT  
		Size: 43.1 MB (43080582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6b413b89640d95a57eb7b842085e6fd4439d390d91cd5d1c4a37e13c30710f`  
		Last Modified: Tue, 02 Jun 2026 07:12:04 GMT  
		Size: 37.7 MB (37687493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365ea1fa2e28b538f48a1a4810554b70175c7cbcfd900d39e942a0067c8b7bb4`  
		Last Modified: Tue, 02 Jun 2026 07:12:08 GMT  
		Size: 226.9 MB (226880728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-24-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:85733fd04435de7e43d12c9572954cdd6784294b39ea76334018cc12b591c6d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159c361e706569be356e9331c8c66e864a819bd1111eb4828ca8c21fcd1c43f6`

```dockerfile
```

-	Layers:
	-	`sha256:86b9b2c2c80128106e99753d5c7e6ac355fe62d6bc9f4972a2d777881a0aa66f`  
		Last Modified: Tue, 02 Jun 2026 07:12:03 GMT  
		Size: 2.4 MB (2366462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e2cc41e29928469e32aa9f5316d5b11c8c99063d12f453607416bf5116267c4`  
		Last Modified: Tue, 02 Jun 2026 07:12:03 GMT  
		Size: 17.9 KB (17850 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-24-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8e6a0aea2e4bda804104559eea071364a97b1d8ecd461b69c76e866820817dc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304086647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a2cf318391be84467d3fc7056eb7fb2605af62abc67c89ae6b5a8fd9bc8308a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:43:55 GMT
ADD oraclelinux-10-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:43:55 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 07:11:22 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 02 Jun 2026 07:11:32 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 02 Jun 2026 07:11:32 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 07:11:32 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 07:11:32 GMT
ENV JAVA_VERSION=27-ea+24
# Tue, 02 Jun 2026 07:11:32 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/24/GPL/openjdk-27-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='eb8d0fac160a096fc406b794465b245a8b40cb1b04bbb4c5824393cde263a8b5'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/24/GPL/openjdk-27-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='832ef5a271052b9065f2b5b7a63ecdbbd0363edd74228736bab7227b45b21a66'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 02 Jun 2026 07:11:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:523b5fcd95921b1880258a8c56e30985e8f3adf21d143bf177907dc76d6a562b`  
		Last Modified: Tue, 12 May 2026 18:44:06 GMT  
		Size: 41.5 MB (41495695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a29592fc483b3f4c221695150f5f9389362613cc717fbc34a247f61c398955f`  
		Last Modified: Tue, 02 Jun 2026 07:11:55 GMT  
		Size: 37.7 MB (37696164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64763745e63ee44cb77154aa917cb6492f750af516c2ad48e6cc1261e3fa0f4`  
		Last Modified: Tue, 02 Jun 2026 07:12:00 GMT  
		Size: 224.9 MB (224894788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-24-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:18e43328367e73f9935d21167c799796a456e851df1e954763b0fc9d4c4a11e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e48ab6aa0722b65ba859e34cd0ae792c2dfba5c1e9cb4152dd9f270c94670c`

```dockerfile
```

-	Layers:
	-	`sha256:9dff09b3be493d2dd5be82d0e77f2bd962785389f7d018c4076f384274e57a57`  
		Last Modified: Tue, 02 Jun 2026 07:11:54 GMT  
		Size: 2.4 MB (2365990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:232964f836fb0fb3a1d4f40e9fbc76b30edf5483ebed631919604a5ec35bec18`  
		Last Modified: Tue, 02 Jun 2026 07:11:53 GMT  
		Size: 18.1 KB (18065 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-24-jdk` - windows version 10.0.26100.32860; amd64

```console
$ docker pull openjdk@sha256:2f1701bcc79424047629f4ec9a6417c7ab4b5c2b4c8316af5925973871872662
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2430281692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f454997fd298e5e5a63354fc03c8d528fa60378135b4d6f539d65c4fbce0ca4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Tue, 02 Jun 2026 07:22:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Jun 2026 07:23:13 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 02 Jun 2026 07:23:14 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 02 Jun 2026 07:23:20 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 02 Jun 2026 07:23:20 GMT
ENV JAVA_VERSION=27-ea+24
# Tue, 02 Jun 2026 07:23:21 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/24/GPL/openjdk-27-ea+24_windows-x64_bin.zip
# Tue, 02 Jun 2026 07:23:21 GMT
ENV JAVA_SHA256=5bbf96e8f91e2c80680961ba7cc2ddb7112131f6fa000d2472ab2ea6c99a06f7
# Tue, 02 Jun 2026 07:24:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 02 Jun 2026 07:24:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b36a0f7c1b88527f3122c1904a3c2a5f59424c7fff771e9086acb32e1f45c706`  
		Last Modified: Tue, 02 Jun 2026 07:24:23 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7bf73508dc8505e08d79e84e50a0e20c6ba5b0444e6ee24d6fda8358a2db3c`  
		Last Modified: Tue, 02 Jun 2026 07:24:23 GMT  
		Size: 430.1 KB (430085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083a7a1446cf1e262ac433bde4d61ed419fab06c207745312b2d9cabb3557313`  
		Last Modified: Tue, 02 Jun 2026 07:24:22 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b506c11d9bbe76029855d3759070d90cae2065f105a5a70554d37d06965d063e`  
		Last Modified: Tue, 02 Jun 2026 07:24:23 GMT  
		Size: 414.2 KB (414188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae9fd377d3ee337b1acbfb3d47d92c26d57168f76083ea9fc96b63f10427aa1`  
		Last Modified: Tue, 02 Jun 2026 07:24:21 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1deaa3ea876cb84ffcdb0d4b2bec65e170299dc034a331db1bfa3d87e66c375b`  
		Last Modified: Tue, 02 Jun 2026 07:24:21 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780c0b3ce0b5af025bb7ace9038dc27ee3922bd9af8d76ce3311068234851b57`  
		Last Modified: Tue, 02 Jun 2026 07:24:21 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec94b2e848c8216c8737d5fc0a7626f677e6df81cfed21473455115aaa602da`  
		Last Modified: Tue, 02 Jun 2026 07:24:35 GMT  
		Size: 223.5 MB (223487891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c08dfeb7e4765495402b9234af1776fe9dac304835494bf9695b553908744e`  
		Last Modified: Tue, 02 Jun 2026 07:24:21 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-24-jdk` - windows version 10.0.20348.5139; amd64

```console
$ docker pull openjdk@sha256:7dbf28a482faed0c5a55339770e70fb131e21761407663d06fd0c539597c2ba2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346617785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46208cefe0d736015511075b5cfde1683a8c4f294d8ae51183708af1c92ed42b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 02 Jun 2026 07:23:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Jun 2026 07:24:39 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 02 Jun 2026 07:24:39 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 02 Jun 2026 07:24:48 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 02 Jun 2026 07:24:48 GMT
ENV JAVA_VERSION=27-ea+24
# Tue, 02 Jun 2026 07:24:49 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/24/GPL/openjdk-27-ea+24_windows-x64_bin.zip
# Tue, 02 Jun 2026 07:24:51 GMT
ENV JAVA_SHA256=5bbf96e8f91e2c80680961ba7cc2ddb7112131f6fa000d2472ab2ea6c99a06f7
# Tue, 02 Jun 2026 07:26:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 02 Jun 2026 07:26:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64818880469c46e82ad7a13b32c2ce7ca26a75a57f681c722c786d77ae355989`  
		Last Modified: Tue, 02 Jun 2026 07:27:07 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53d4dc39f0640e55c3246822ffcb42aafcc08ad3a3eb7629646b3bd522d73fe`  
		Last Modified: Tue, 02 Jun 2026 07:27:08 GMT  
		Size: 496.7 KB (496678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144ebb81ce7ea3e28ce5b655bc8f39163f288ae22b1141bd8ae67d3c667b981d`  
		Last Modified: Tue, 02 Jun 2026 07:27:07 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c7e3f786aa934c6e5c7de54c20ee4ec0ea0e9b26e7879f69c4d45154f3f2564`  
		Last Modified: Tue, 02 Jun 2026 07:27:07 GMT  
		Size: 306.8 KB (306777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b661042879ba25b28496c7bd43a136631ccf4ac8c0229877c3927199465c4ec1`  
		Last Modified: Tue, 02 Jun 2026 07:27:05 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9cd8e6b2dd3744242ef2e0ff3a064f3dbf4b01ede0ead6f6a02094e263ee0b9`  
		Last Modified: Tue, 02 Jun 2026 07:27:06 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f8a72306f096bdad2e5f21cdb529f265a94f9f1fdd78b0ab5e0fba81941c330`  
		Last Modified: Tue, 02 Jun 2026 07:27:06 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253fe32c239c42008c8466a0b99de8b9a51b8e76427658d9e8fd5bfd59f76dd0`  
		Last Modified: Tue, 02 Jun 2026 07:27:21 GMT  
		Size: 223.4 MB (223385898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3981e2a59ead14b875308e79ce71201777cdf7a971f454ef5fede776a77129`  
		Last Modified: Tue, 02 Jun 2026 07:27:06 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
