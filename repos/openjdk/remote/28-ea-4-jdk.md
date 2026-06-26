## `openjdk:28-ea-4-jdk`

```console
$ docker pull openjdk@sha256:cd738828fd11fce1311d90473da351b23ed94842b6c3372af10d8e07497e0a88
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.32995; amd64
	-	windows version 10.0.20348.5256; amd64

### `openjdk:28-ea-4-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:37180c9fbdb053aacf7c7f343d4c26a4f40c0fa9932a658918613b30556efb80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.2 MB (308187586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f458263639edf737252edc99385ef41c86854a940fc46e10a17c86267dd43e76`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:44:08 GMT
ADD oraclelinux-10-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:08 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:49:34 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 26 Jun 2026 17:49:44 GMT
ENV JAVA_HOME=/usr/java/openjdk-28
# Fri, 26 Jun 2026 17:49:44 GMT
ENV PATH=/usr/java/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jun 2026 17:49:44 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jun 2026 17:49:44 GMT
ENV JAVA_VERSION=28-ea+4
# Fri, 26 Jun 2026 17:49:44 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/4/GPL/openjdk-28-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='3f349a9ae39761069b8132f7ba529bec7bf6c759376f77cb57520d3f21d4fa23'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/4/GPL/openjdk-28-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='a49e869b72df691c734d29e133fd15ae49bed271913327704c9bca6c2132525d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jun 2026 17:49:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ded2aa0abafd1e1e93e05338cb1b14916dbeb283d3862aa21e5d8b0164f4cbf3`  
		Last Modified: Tue, 12 May 2026 18:44:20 GMT  
		Size: 43.1 MB (43080582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f33c2767f1258249fd3138c95a77cdf445ec500d0b72cdf0ec80865c4307258`  
		Last Modified: Fri, 26 Jun 2026 17:50:08 GMT  
		Size: 37.7 MB (37687216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922b47249f9035226eaeb47c8f23353dad870b8f258d8fe217299c1277f452dc`  
		Last Modified: Fri, 26 Jun 2026 17:50:11 GMT  
		Size: 227.4 MB (227419788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-4-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:9ac06dd12ba203fc9513dd276f5f19e86fc8a89c018702e5f0837a86b2c10de3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff6ad553a6b1455917b09f8a54b14472f710b59f795457ae77b4018eb7fa02a8`

```dockerfile
```

-	Layers:
	-	`sha256:c48b4d392f2b43f1a0cc64be9478bf21cc7390a589aecbd38ee7cd58b11fa80a`  
		Last Modified: Fri, 26 Jun 2026 17:50:05 GMT  
		Size: 2.4 MB (2366446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82f3fed06784e3bf0c2264af1dd9f66e81b4f786cadfbd11810112f3b078b33d`  
		Last Modified: Fri, 26 Jun 2026 17:50:05 GMT  
		Size: 17.8 KB (17829 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:28-ea-4-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a89069ac1e79f38f26139c356f4ff8630d71e48a4c75d023f1beba157ceabe91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.6 MB (304644295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55d06178dce04af775c7155ae93f2119124284c6a58e39b3199e155285d5a69`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:43:55 GMT
ADD oraclelinux-10-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:43:55 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:54:35 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 26 Jun 2026 17:54:47 GMT
ENV JAVA_HOME=/usr/java/openjdk-28
# Fri, 26 Jun 2026 17:54:47 GMT
ENV PATH=/usr/java/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jun 2026 17:54:47 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jun 2026 17:54:47 GMT
ENV JAVA_VERSION=28-ea+4
# Fri, 26 Jun 2026 17:54:47 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/4/GPL/openjdk-28-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='3f349a9ae39761069b8132f7ba529bec7bf6c759376f77cb57520d3f21d4fa23'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/4/GPL/openjdk-28-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='a49e869b72df691c734d29e133fd15ae49bed271913327704c9bca6c2132525d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jun 2026 17:54:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:523b5fcd95921b1880258a8c56e30985e8f3adf21d143bf177907dc76d6a562b`  
		Last Modified: Tue, 12 May 2026 18:44:06 GMT  
		Size: 41.5 MB (41495695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6874a711555de5763ac0a1baf87290916d7b912ed089634e4042b6e9aa672b6`  
		Last Modified: Fri, 26 Jun 2026 17:55:10 GMT  
		Size: 37.7 MB (37695940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd72f79b37847e8a9f4c0dc38f246594dc4020e19bb20cc4c972b19fd81804aa`  
		Last Modified: Fri, 26 Jun 2026 17:55:14 GMT  
		Size: 225.5 MB (225452660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-4-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:13da6a2631ca0165f301f8b397bc5e2f673a31890c4d66ee3746bb5974aaeb70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab83a7011a582d9db3e5005ee630b2b477b299844a7503420779bde1c3c25963`

```dockerfile
```

-	Layers:
	-	`sha256:23cd1a91e1fa5d076c719946feb0b94b86c9e1e2aa311d9e4e580f71edb0e8c8`  
		Last Modified: Fri, 26 Jun 2026 17:55:09 GMT  
		Size: 2.4 MB (2365974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bf953469b994e9f78be82cbc40fc4a24e7e514b4cd64b9cd534549a7108a86f`  
		Last Modified: Fri, 26 Jun 2026 17:55:08 GMT  
		Size: 18.0 KB (18044 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:28-ea-4-jdk` - windows version 10.0.26100.32995; amd64

```console
$ docker pull openjdk@sha256:0b17e008ecd8cf67c4817fa90bc1deb2d695185c7330de77390bc33353d87664
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2504406076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5dfa3571b598e3029eeab9660054c23f8aa485020824e4c59f6d7d622698180`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Fri, 26 Jun 2026 22:42:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 26 Jun 2026 22:43:25 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 26 Jun 2026 22:43:26 GMT
ENV JAVA_HOME=C:\openjdk-28
# Fri, 26 Jun 2026 22:43:32 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 26 Jun 2026 22:43:32 GMT
ENV JAVA_VERSION=28-ea+4
# Fri, 26 Jun 2026 22:43:33 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk28/4/GPL/openjdk-28-ea+4_windows-x64_bin.zip
# Fri, 26 Jun 2026 22:43:34 GMT
ENV JAVA_SHA256=b85f4b0c1313453fc760c198dec39f0c3a27e386671a184a123c19fcfb46c776
# Fri, 26 Jun 2026 22:44:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 26 Jun 2026 22:44:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee71d57b2226db82d002abc39a97b7dd144f007db435566364a0285bf115b83`  
		Last Modified: Tue, 09 Jun 2026 18:08:12 GMT  
		Size: 756.1 MB (756083682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8e4546b69fc08bed7bcc81486904a224e3a5e52d2a8c4dca141adca5ee5ce0`  
		Last Modified: Fri, 26 Jun 2026 22:44:07 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff609767754f9b924164651999bae6286a7bd48f87a9139fa1eb36a0a6bcd768`  
		Last Modified: Fri, 26 Jun 2026 22:44:07 GMT  
		Size: 402.6 KB (402571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ac0af4c28df97ed46f78c867f8ab2a0447ccf0fdb07fe6d3e26d8325d34144`  
		Last Modified: Fri, 26 Jun 2026 22:44:07 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9ae7cb620fb920cd95bfea7f2a20fbf67082af59603aba342d7ce75cf50d4be`  
		Last Modified: Fri, 26 Jun 2026 22:44:07 GMT  
		Size: 390.1 KB (390092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c12e28cb48b30bc7ad092e94270c725615e04db0a8fbffeb1b2bec412dab5e0`  
		Last Modified: Fri, 26 Jun 2026 22:44:05 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d342bd7ab30f17d3e1815b1a3e603bd9d90c1cd960a60755f0c855d14e8fbc10`  
		Last Modified: Fri, 26 Jun 2026 22:44:05 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:700ef82c47bc6ae276429173436bccfc7077070927b9be5628bcb3e03e3b896d`  
		Last Modified: Fri, 26 Jun 2026 22:44:05 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2b2c841cff667bb27278ef8709950bcf2b685c6567e0416a71e57055eeb54f`  
		Last Modified: Fri, 26 Jun 2026 22:44:21 GMT  
		Size: 224.5 MB (224462685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b2b7c40675f1a3dc7dff1cbbf73c32eff9455e61e9132903d565e1d93c2953`  
		Last Modified: Fri, 26 Jun 2026 22:44:05 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:28-ea-4-jdk` - windows version 10.0.20348.5256; amd64

```console
$ docker pull openjdk@sha256:38775a76a4ab6261a6a863489534dfe43f2fd07dcdbf6f9b127178c8e8d54919
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2357421003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15822d9500cf82d9d5c2b4a681e541dc723572976130bf954b7993ace7368511`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Fri, 26 Jun 2026 22:43:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 26 Jun 2026 22:43:54 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 26 Jun 2026 22:43:55 GMT
ENV JAVA_HOME=C:\openjdk-28
# Fri, 26 Jun 2026 22:44:02 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 26 Jun 2026 22:44:02 GMT
ENV JAVA_VERSION=28-ea+4
# Fri, 26 Jun 2026 22:44:03 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk28/4/GPL/openjdk-28-ea+4_windows-x64_bin.zip
# Fri, 26 Jun 2026 22:44:04 GMT
ENV JAVA_SHA256=b85f4b0c1313453fc760c198dec39f0c3a27e386671a184a123c19fcfb46c776
# Fri, 26 Jun 2026 22:45:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 26 Jun 2026 22:45:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6abaff06b6cf8d216a7cd97ba106d8b7fff77fd20dd23f8b011085d795dedb`  
		Last Modified: Fri, 26 Jun 2026 22:45:59 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce2cd747a577ffed1599ea67899827f4db92db1edeae4f67de272e5fec1d0cf`  
		Last Modified: Fri, 26 Jun 2026 22:45:59 GMT  
		Size: 502.9 KB (502856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9090a0352da1996214a8fc740c6e23e2bbab6dde1ced339c3c0b30fe72be7a0d`  
		Last Modified: Fri, 26 Jun 2026 22:45:58 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a32ad2d94825c4e1b134e3e5a48ac35fa1f98a908728fde6a270b03206734890`  
		Last Modified: Fri, 26 Jun 2026 22:45:59 GMT  
		Size: 351.9 KB (351886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d8dfb02e6af436f55e266423d5e1f045a2abfe1323986f43c65c859adbc409`  
		Last Modified: Fri, 26 Jun 2026 22:45:57 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9021843611160965c7d4201b79f6336006a9efe82a335d80018c89cd0ab5d579`  
		Last Modified: Fri, 26 Jun 2026 22:45:57 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54537bdf3282a6b77f0c47bed33d2064bc1f0c8749582a664f3d812a42853c70`  
		Last Modified: Fri, 26 Jun 2026 22:45:57 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1b2d5f8e0e7c7ff167c844a2dc9eb050cd4509e8c322ca9776804ea2e1bea7`  
		Last Modified: Fri, 26 Jun 2026 22:46:13 GMT  
		Size: 224.4 MB (224432834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3007c94ba763e47716d2e6ef9ff6e6e85f6cec5fc92654f983ab8b544cd4d1`  
		Last Modified: Fri, 26 Jun 2026 22:45:57 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
