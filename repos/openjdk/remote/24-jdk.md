## `openjdk:24-jdk`

```console
$ docker pull openjdk@sha256:9c5eba61314c725a538920332c382cca9ac26ddd5cb53ae551acd4189950271b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.20348.2527; amd64
	-	windows version 10.0.17763.5936; amd64

### `openjdk:24-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:53109ca4df8989f0e9b99028fcd2bddafe29cbc8d01ae74fc21f9ca215a20651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.2 MB (298197257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d444e96ecbee110a0d9ecd94cd45a532424d49b533fded25cb4074be98e0b4d`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 01 Jun 2024 00:47:59 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Sat, 01 Jun 2024 00:48:00 GMT
CMD ["/bin/bash"]
# Tue, 11 Jun 2024 06:58:53 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 11 Jun 2024 06:58:53 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Tue, 11 Jun 2024 06:58:53 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Jun 2024 06:58:53 GMT
ENV LANG=C.UTF-8
# Tue, 11 Jun 2024 06:58:53 GMT
ENV JAVA_VERSION=24-ea+1
# Tue, 11 Jun 2024 06:58:53 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/1/GPL/openjdk-24-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='8548b9f8147e53846600a5afd39adb7f3f50a226edeb12e336d43837708f0dfe'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/1/GPL/openjdk-24-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='d98e475916eb68814f1ddacc0ba56128025a829351b7bc51e4b4b862cf12d5fb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 11 Jun 2024 06:58:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dac3e7a7894e1f152fef3ceea49f758a9134375e11651bfef76daabcbe30c2e`  
		Last Modified: Wed, 12 Jun 2024 00:55:28 GMT  
		Size: 37.9 MB (37862346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3983018790f8a4853f62b2c3e4f77564cea2d829393bd63ce4f2654b17347c`  
		Last Modified: Wed, 12 Jun 2024 00:55:30 GMT  
		Size: 211.3 MB (211340033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:292914f5cc6fea0c26678df52c4f06fe7975f7bdd4ff577714fdc686f0f569e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3352728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7feae9fee59972d43a9bf743ff6b5ddac11b957fb65198b7d6434563270dd17`

```dockerfile
```

-	Layers:
	-	`sha256:840fa447018054a17c07ec502938be29d2b7b3c9d13b71565d5f0375a8521a49`  
		Last Modified: Wed, 12 Jun 2024 00:55:27 GMT  
		Size: 3.3 MB (3333225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9db05f006aa673c6b67f8cf1ce87bf0274b91a0ff0649ede120d5c7b353cd113`  
		Last Modified: Wed, 12 Jun 2024 00:55:27 GMT  
		Size: 19.5 KB (19503 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:dd7c6028b974c418d53be2da62804679d2d1bd40d4221919914cbde89abaf781
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295131743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5cdf3011367375ac6f195ad44651481697846c77b3169dba8246b4120f3e7d`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 01 Jun 2024 01:47:52 GMT
ADD file:e2d1c7a0eab3573f307b1affb1e88a1c24614b2ec92eb17723bc07cfa2083423 in / 
# Sat, 01 Jun 2024 01:47:53 GMT
CMD ["/bin/bash"]
# Tue, 11 Jun 2024 06:58:53 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 11 Jun 2024 06:58:53 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Tue, 11 Jun 2024 06:58:53 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Jun 2024 06:58:53 GMT
ENV LANG=C.UTF-8
# Tue, 11 Jun 2024 06:58:53 GMT
ENV JAVA_VERSION=24-ea+1
# Tue, 11 Jun 2024 06:58:53 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/1/GPL/openjdk-24-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='8548b9f8147e53846600a5afd39adb7f3f50a226edeb12e336d43837708f0dfe'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/1/GPL/openjdk-24-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='d98e475916eb68814f1ddacc0ba56128025a829351b7bc51e4b4b862cf12d5fb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 11 Jun 2024 06:58:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:da7a98631edf9304544ff835ff2891b9c7a6773ae8a8bbd8041b6ef3af01fae9`  
		Last Modified: Sat, 01 Jun 2024 01:49:25 GMT  
		Size: 47.7 MB (47651991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4126ceeefbe5a1d06272578a6b6a99a1d422489b25511cbccbaaeb1576551bfd`  
		Last Modified: Sun, 02 Jun 2024 01:54:26 GMT  
		Size: 38.3 MB (38259157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0618ad044643ca31138a43cd8e7de71086151d7e9479f075a9c3daeedb0fc0f`  
		Last Modified: Wed, 12 Jun 2024 01:47:21 GMT  
		Size: 209.2 MB (209220595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:5c72be83e6cec76372b88ecf4546a120f7554525a4b677ea0b79a3b8e4e39990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3351586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:450c7de385bc3a0946fda90353889a36dfa035508844aefafdd7c25210644b43`

```dockerfile
```

-	Layers:
	-	`sha256:c4969f4f3ebd9c7e670fe34cb1b727403f5405d35241d0207d37c551c439e146`  
		Last Modified: Wed, 12 Jun 2024 01:47:17 GMT  
		Size: 3.3 MB (3331608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cdc44e9ad48c6c8ceacd45c56cb5cdc8c0892cb1358b20a16d888f6e4e465d5`  
		Last Modified: Wed, 12 Jun 2024 01:47:16 GMT  
		Size: 20.0 KB (19978 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk` - windows version 10.0.20348.2527; amd64

```console
$ docker pull openjdk@sha256:b81d9001c7bf1106935a1c5fd59a9c4d8aaedeead3cd16d014ac1a0965de282d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2325366025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d49b019541c398e9dd198d5d1491ec078d3cc72948b5729e5427389a21b45a74`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 07 Jun 2024 09:02:12 GMT
RUN Install update 10.0.20348.2527
# Wed, 12 Jun 2024 18:06:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jun 2024 18:06:20 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 12 Jun 2024 18:06:20 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 12 Jun 2024 18:06:26 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 12 Jun 2024 18:06:26 GMT
ENV JAVA_VERSION=24-ea+1
# Wed, 12 Jun 2024 18:06:27 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/1/GPL/openjdk-24-ea+1_windows-x64_bin.zip
# Wed, 12 Jun 2024 18:06:28 GMT
ENV JAVA_SHA256=84640da466dc6c7af5dbd523e321f5cfef6b81a434c1558b43633e7485da95f7
# Wed, 12 Jun 2024 18:06:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 12 Jun 2024 18:06:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedf08888525e83e4a050655b4ec0d81647e59a69f7007a560df774a656da9bb`  
		Last Modified: Tue, 11 Jun 2024 17:49:21 GMT  
		Size: 729.6 MB (729579921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb8f7f1748cabfa2e0b5c55969b2e4d22819bce47a87730a69347e03ae38188b`  
		Last Modified: Wed, 12 Jun 2024 18:06:52 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf3590495ca430c4cb9bd4cd7838d752782b474c64c4e3005d0f32926e6516f8`  
		Last Modified: Wed, 12 Jun 2024 18:06:53 GMT  
		Size: 358.7 KB (358715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556aa7dba34c013165b3878a16bca9b43102749f263246355fe5ca40b42726ec`  
		Last Modified: Wed, 12 Jun 2024 18:06:52 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e380f248928c89d79064d6fb675a67bde544886ec6d76fe41c17b61ca6392c6`  
		Last Modified: Wed, 12 Jun 2024 18:06:52 GMT  
		Size: 342.4 KB (342386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f34077c0578498e782c125233639004653b185a85b8cfa000c8b2ed677e8be4`  
		Last Modified: Wed, 12 Jun 2024 18:06:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4296f2b2dd1c6e784a1d5a56ef8290e17c721e82a68bf7193bf134351eae9da`  
		Last Modified: Wed, 12 Jun 2024 18:06:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c616546812b276722ba029f7739344370788c9b3aa9a074586817a6bbae683d1`  
		Last Modified: Wed, 12 Jun 2024 18:06:51 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd30cfe57bfe9955fc12dfc40bffe875446c4ed2faf14a359891f8913a2c4bf`  
		Last Modified: Wed, 12 Jun 2024 18:07:02 GMT  
		Size: 206.5 MB (206478509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f8922c47401eadc602be4c1a2bbe1d2c7a8e10e308903d8733ddb07e02d39f`  
		Last Modified: Wed, 12 Jun 2024 18:06:51 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-jdk` - windows version 10.0.17763.5936; amd64

```console
$ docker pull openjdk@sha256:a00dfee83acbfc93ecc4649c89628ec0627eacda6aa0563e8856ecfedb1bbfa8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2427962910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:503f0d557140ecab09bb5db3bbfe48df6266b2073a070c6a853f39d13fb0bed9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Wed, 12 Jun 2024 18:15:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jun 2024 18:16:52 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 12 Jun 2024 18:16:53 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 12 Jun 2024 18:17:12 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 12 Jun 2024 18:17:13 GMT
ENV JAVA_VERSION=24-ea+1
# Wed, 12 Jun 2024 18:17:14 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/1/GPL/openjdk-24-ea+1_windows-x64_bin.zip
# Wed, 12 Jun 2024 18:17:14 GMT
ENV JAVA_SHA256=84640da466dc6c7af5dbd523e321f5cfef6b81a434c1558b43633e7485da95f7
# Wed, 12 Jun 2024 18:17:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 12 Jun 2024 18:17:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559b7a7993ffd5e1b96aba469916c6d8fabc5ef877eaaba5ba7c3c976f1c42cb`  
		Last Modified: Wed, 12 Jun 2024 18:17:54 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4a4b9104dad18aa6b339c045a214e7337c24343be05fadaff0b8783393e3c5c`  
		Last Modified: Wed, 12 Jun 2024 18:17:55 GMT  
		Size: 475.0 KB (475014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b88b81a77ecb7a8822734017801f1bef0d60eceae01bd8e536f6268c7af7b36`  
		Last Modified: Wed, 12 Jun 2024 18:17:54 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653f4b54e17863fe7d174fb00c45be7f75d07cfb1c73fc4406c1a029b845da52`  
		Last Modified: Wed, 12 Jun 2024 18:17:55 GMT  
		Size: 322.8 KB (322784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc109fce1e7d6d1c7aff0e9598b5497afd5368ffda2a1f28fbd2acfcfeeff509`  
		Last Modified: Wed, 12 Jun 2024 18:17:53 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc9b4a3d65aee8778712b23d5d19e4e16e3c9e0ca21aff1bb9ac6d3501ddc9c`  
		Last Modified: Wed, 12 Jun 2024 18:17:53 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dfdefd97289f13704e3fc93f2c87137d5a604cbb4f999fe1fd6b299fd233a45`  
		Last Modified: Wed, 12 Jun 2024 18:17:53 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7397b9b8e070bc9ad6133b761b3e26a01f2a8a46c763fd5718ce7e148b89b948`  
		Last Modified: Wed, 12 Jun 2024 18:18:04 GMT  
		Size: 206.5 MB (206475972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0dc625f5db20c918bf5322be2af99a668d6084b18a4b3dfc9fb14851a8c218`  
		Last Modified: Wed, 12 Jun 2024 18:17:53 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
