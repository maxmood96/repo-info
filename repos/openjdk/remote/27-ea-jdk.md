## `openjdk:27-ea-jdk`

```console
$ docker pull openjdk@sha256:9f7fa8875698170e6e5c5614bbec42fadce0e56e1ee11c1aec64038e9474ec8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.32370; amd64
	-	windows version 10.0.20348.4773; amd64

### `openjdk:27-ea-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:8330d2eb6d3d3733d54d6313d07d277ab7cedcba4e47a55aa81f30baf20a4d00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (313973083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6223698c3ed0dc44f01c47856d0ad0dfc3e70463164e4b09f004a0f707a5d901`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Feb 2026 19:11:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:11:41 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:38:27 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:38:36 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Thu, 19 Feb 2026 19:38:36 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Feb 2026 19:38:36 GMT
ENV LANG=C.UTF-8
# Thu, 19 Feb 2026 19:38:36 GMT
ENV JAVA_VERSION=27-ea+9
# Thu, 19 Feb 2026 19:38:36 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/9/GPL/openjdk-27-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='63b3704a0d6aac8050df9534d12f1e063e64ceae89a77131e1a9f01e0d1e223b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/9/GPL/openjdk-27-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='58393a7f38ddf3532c68f68b614756b3cb7953bbd54e64897221be7f071ee41b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 19 Feb 2026 19:38:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:74a8e4bbd9fe8a9fb7df9f028398fc37d20efc1cde6bf66eeeabef7755e5f5fe`  
		Last Modified: Thu, 19 Feb 2026 19:11:53 GMT  
		Size: 47.3 MB (47308871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e68466e7cb33ce0944f33391420e5b0f1895d23c7000c5c4f12ab96a04b5e4a`  
		Last Modified: Thu, 19 Feb 2026 19:39:00 GMT  
		Size: 38.3 MB (38296194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04601720671448427e66a7bfaa606272a4a42d7c06067602a11e8fdd79d9e1bb`  
		Last Modified: Thu, 19 Feb 2026 19:39:05 GMT  
		Size: 228.4 MB (228368018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:acfe4ba32ebc27bfbda42041122638bd73d3844a7a7a8b19b2544212f7f21f45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a2fce7f814503d0e88f2ebd13bfc727d0af38803b16ac4b08e83564b20c5a54`

```dockerfile
```

-	Layers:
	-	`sha256:85a04a4c076d48c9c74bc769983d72e1e2466513a5e851fe2a7cdad4fb0414cf`  
		Last Modified: Thu, 19 Feb 2026 19:38:58 GMT  
		Size: 3.7 MB (3655421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44d57e908c5c3b1239fc35f840e2fd32d3e0c7d31c41a2f395700e0393d54771`  
		Last Modified: Thu, 19 Feb 2026 19:38:58 GMT  
		Size: 17.8 KB (17814 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:5efb48e20be10aaf62af3aaea21961a6e24518e491a48de5a4414d4ba4e7ce8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.9 MB (310908583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67d73282fbd8602aa69b9d70a96f867ff5da00bd51b7f15ea32308a91649d1c6`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Feb 2026 19:06:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:06:57 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:55 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:38:05 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Thu, 19 Feb 2026 19:38:05 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Feb 2026 19:38:05 GMT
ENV LANG=C.UTF-8
# Thu, 19 Feb 2026 19:38:05 GMT
ENV JAVA_VERSION=27-ea+9
# Thu, 19 Feb 2026 19:38:05 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/9/GPL/openjdk-27-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='63b3704a0d6aac8050df9534d12f1e063e64ceae89a77131e1a9f01e0d1e223b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/9/GPL/openjdk-27-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='58393a7f38ddf3532c68f68b614756b3cb7953bbd54e64897221be7f071ee41b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 19 Feb 2026 19:38:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:482e8d56575a6fbe539cfb44150fa96593766f3af0610165cb5c8a63fa68d8db`  
		Last Modified: Thu, 19 Feb 2026 19:07:09 GMT  
		Size: 45.9 MB (45901980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d54dce5ddeb617a42d78e887ced87b7680614f70c5eb164e124957c312d42f`  
		Last Modified: Thu, 19 Feb 2026 19:38:29 GMT  
		Size: 38.7 MB (38693415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57484575fbe404e7fb9194a3d0a255a366bc983916d3e7020a150e0f4b25e27f`  
		Last Modified: Thu, 19 Feb 2026 19:38:33 GMT  
		Size: 226.3 MB (226313188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:9e54731c2c3a0665af1aaf5084fb919bd60a53ac7d5c51847f898fe7a04ef2e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1421c3b25065c9bf90220af3ce2421741879161980689ffed1e35bd146ff0e9b`

```dockerfile
```

-	Layers:
	-	`sha256:f716246f175a6612c1505dc9e753a9757e0e9f57aaae8b554ced85b6b3329f0c`  
		Last Modified: Thu, 19 Feb 2026 19:38:27 GMT  
		Size: 3.7 MB (3653111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5d93fc1b1de080ade7217d6af31e405d274a38cfb95e33f3f6622c454793b57`  
		Last Modified: Thu, 19 Feb 2026 19:38:27 GMT  
		Size: 18.0 KB (18029 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk` - windows version 10.0.26100.32370; amd64

```console
$ docker pull openjdk@sha256:5985fc0e4ab580eae9b1c39d066a72d8cd303afc2abeb0d96b690585a231ff3a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2190361780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:599980f6181742f82ab596f186a6601e5ad705fd95fb40412a2306278b74ecb7`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Feb 2026 22:21:49 GMT
RUN Install update 10.0.26100.32370
# Tue, 17 Feb 2026 19:27:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 17 Feb 2026 19:27:22 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 17 Feb 2026 19:32:46 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 17 Feb 2026 19:32:51 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 17 Feb 2026 19:32:51 GMT
ENV JAVA_VERSION=27-ea+9
# Tue, 17 Feb 2026 19:32:52 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/9/GPL/openjdk-27-ea+9_windows-x64_bin.zip
# Tue, 17 Feb 2026 19:32:52 GMT
ENV JAVA_SHA256=8f50a6f1fbb252ea650c31da6e40bdd95a1b286d715b84748ef20d251ac46b76
# Tue, 17 Feb 2026 19:33:16 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 17 Feb 2026 19:33:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456534216d0c12d9314cda831989d54bb3f542d7d43d9772ba40654db6dbd7bc`  
		Last Modified: Tue, 10 Feb 2026 18:52:01 GMT  
		Size: 441.7 MB (441700471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47376505e9774f463250f38092b0512796232df85683d4e85beeb9bfb4eb1563`  
		Last Modified: Tue, 17 Feb 2026 19:28:02 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f65ca361387030a79fd0a8b6bce97ba03d6f4c05eafab7bbb336b0cc8f197cd`  
		Last Modified: Tue, 17 Feb 2026 19:28:02 GMT  
		Size: 382.4 KB (382425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a3d2efb5f3de8eb070c292173985fec703d3164365588ac24efb5193c82d6ae`  
		Last Modified: Tue, 17 Feb 2026 19:33:24 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970fc10841555fb4d3116301e24ceeb7c32e0d954d96730437094aaa1e2ce035`  
		Last Modified: Tue, 17 Feb 2026 19:33:24 GMT  
		Size: 370.7 KB (370720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f8f6a438e5c03cdaf6f60a3d3e0545c801cf8832032c0bae7bd34aaaa3b2d24`  
		Last Modified: Tue, 17 Feb 2026 19:33:22 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13473e3e2be3d1256eb47d0ac6ae4c9c2e68038a7b632daaceb91cb879351115`  
		Last Modified: Tue, 17 Feb 2026 19:33:22 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71bf13050a823b7e242fe212cd8fc3c40facec7534908154c45e25205f5f9082`  
		Last Modified: Tue, 17 Feb 2026 19:33:22 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbae85cc3137429a1e439744dcbb4637ba5252bba431cdfe779faa94870d0b0`  
		Last Modified: Tue, 17 Feb 2026 19:33:37 GMT  
		Size: 224.8 MB (224840872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9215a7d8fe27da41f4dcf03e070393a524a17180deade4db6d0e9abae12ad19`  
		Last Modified: Tue, 17 Feb 2026 19:33:22 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-jdk` - windows version 10.0.20348.4773; amd64

```console
$ docker pull openjdk@sha256:8b1a0b7e57c8b28fa80c63d0c17d41ef96d7b0a81d8bb3075ad4b0013f0cd6c2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2088342551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f2ec5a0ca6d92f80bf677b7248049284b8c79cf4d8df31b560432b16e4ad768`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Tue, 17 Feb 2026 19:45:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 17 Feb 2026 19:46:12 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 17 Feb 2026 19:58:49 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 17 Feb 2026 19:58:55 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 17 Feb 2026 19:58:55 GMT
ENV JAVA_VERSION=27-ea+9
# Tue, 17 Feb 2026 19:58:56 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/9/GPL/openjdk-27-ea+9_windows-x64_bin.zip
# Tue, 17 Feb 2026 19:58:57 GMT
ENV JAVA_SHA256=8f50a6f1fbb252ea650c31da6e40bdd95a1b286d715b84748ef20d251ac46b76
# Tue, 17 Feb 2026 19:59:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 17 Feb 2026 19:59:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:537c87dc79dd0988a4104b7c89e38ad000e2354ad04b242a5e7c0febe517e1f7`  
		Last Modified: Tue, 17 Feb 2026 19:47:41 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c365cc66df2c402fb4def346ed016c3253688d4764a39dce6906f20709c0f815`  
		Last Modified: Tue, 17 Feb 2026 19:47:41 GMT  
		Size: 505.6 KB (505601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e8f9796fc1887885cc90473ef01c9e2773b481187a4c7f88c4ec761b42b9f9`  
		Last Modified: Tue, 17 Feb 2026 19:59:41 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7039622b8be9e454036a24447b09c505f9aa34293f90a26c9d15cc3c85dca6a1`  
		Last Modified: Tue, 17 Feb 2026 19:59:42 GMT  
		Size: 352.1 KB (352082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df39cfe705319acf93de6479e46e5c2c5dfd131965df09e9dd765b4ec49babb`  
		Last Modified: Tue, 17 Feb 2026 19:59:40 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b23b9b389d8a647920ffbba6e34fadc6a53c46925b180380498281a5aa10057`  
		Last Modified: Tue, 17 Feb 2026 19:59:40 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd5282b2e3b2a2d42d23592bcefa4f0e3cb58f0d268ef37c0437180273038b64`  
		Last Modified: Tue, 17 Feb 2026 19:59:40 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23c9a1a65046399f5211b933f037d06af10146795ec7dc47e317920081bc3a5`  
		Last Modified: Tue, 17 Feb 2026 19:59:55 GMT  
		Size: 224.8 MB (224819860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af0511a3c4c58c2d8a53e7a5199c959937a95a7c5406786ce68a3aa5471a407c`  
		Last Modified: Tue, 17 Feb 2026 19:59:40 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
