## `openjdk:23-jdk`

```console
$ docker pull openjdk@sha256:3f8fc0250125e57176601a2bb8d7af95ccd338d9f1e53bbfe4a0f499c1fba807
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.20348.2529; amd64
	-	windows version 10.0.17763.5936; amd64

### `openjdk:23-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:7d85d6356d6b8f7890d64d98ba9ea47d2c4ced5f98e72a9a31350c42c22349ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.2 MB (298157327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8d32c8acbc7ab384ea9cd3cb76fafe49ff59bf0b8094b19f6a81ef4ef4f27db`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
CMD ["/bin/bash"]
# Sat, 29 Jun 2024 00:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 29 Jun 2024 00:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Sat, 29 Jun 2024 00:48:10 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 29 Jun 2024 00:48:10 GMT
ENV LANG=C.UTF-8
# Sat, 29 Jun 2024 00:48:10 GMT
ENV JAVA_VERSION=23-ea+29
# Sat, 29 Jun 2024 00:48:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/29/GPL/openjdk-23-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='1ecb4977a7385dde5f7155e22cfdad0bec51afb8ff4dece08a061bab64be8aaa'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/29/GPL/openjdk-23-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='a14bddc20e706cf85f28b8cc360e3dc2506b51cff9a0e62125f3213de6c41f00'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 29 Jun 2024 00:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a523cc422854f5fe352c82d3c00dbe4242724550d6bce00ca506ddf79528443`  
		Last Modified: Tue, 02 Jul 2024 00:57:54 GMT  
		Size: 37.9 MB (37862552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab1f912018b0e1097fdf49845e3df2416c5dd41333f1697902f7ac1f7d29c3f`  
		Last Modified: Tue, 02 Jul 2024 00:57:58 GMT  
		Size: 211.3 MB (211301122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:f543691b2a3ad7663c8b3074ac8a8f811cd681cf4467561e3bf072dc5da8c848
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3352772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbbad3968a36cea99d9f61b3bb6c722e58d3c23a99e3097e63169455402d9b5a`

```dockerfile
```

-	Layers:
	-	`sha256:99f7bb3cfeb63b08fd6f4f570177f41ef2ff18bdf9a33f1267b703dc78b3e753`  
		Last Modified: Tue, 02 Jul 2024 00:57:54 GMT  
		Size: 3.3 MB (3333244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98a7ac16d7077c9e0c7b1e52e24258f38b88a795d0cfbdab0adcac83c9bd8571`  
		Last Modified: Tue, 02 Jul 2024 00:57:53 GMT  
		Size: 19.5 KB (19528 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7e66549403a4202818bbef2a5333c6f76fcce8e282583a47639c4cfbc932ee4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295069532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5c583763d8361fadc7a101e9ebfff3453b8f9ddec265c4ac61dc328718d4a3d`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 21 Jun 2024 18:48:11 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Fri, 21 Jun 2024 18:48:11 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 18:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 21 Jun 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 21 Jun 2024 18:48:11 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Jun 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 21 Jun 2024 18:48:11 GMT
ENV JAVA_VERSION=23-ea+28
# Fri, 21 Jun 2024 18:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/28/GPL/openjdk-23-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='55c6ef3457ea9e056119ae7ab55e4691742458d74fbe1a1a7cdb7d08527bee1f'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/28/GPL/openjdk-23-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='9844e3616fd6e16a94212badb2aee65f0a5805b43c587d80e9ae85174f18b984'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 21 Jun 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e03e86442d91879ee632bd4444507fcf4dadd66cc8c2b8458e11db03d0883c`  
		Last Modified: Fri, 21 Jun 2024 20:58:16 GMT  
		Size: 38.3 MB (38256430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98fa5e082abff7131f0f2d9b2912842e42e3e9089ce3503b0b6aad43cb3c839`  
		Last Modified: Sat, 22 Jun 2024 06:21:23 GMT  
		Size: 209.2 MB (209160336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:884a573e87161b0d614ee83ce199316212c611f2a7ad22494966cbc5c383477e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3351630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1db526da79ac6b1070d344f0a9442e679ebb3217a439bc05aeaf5aa74411a5`

```dockerfile
```

-	Layers:
	-	`sha256:ef69cecfa94d915b8ed6ce7351640abdac94b108c03a720d4fe9695b6d91d3e5`  
		Last Modified: Sat, 22 Jun 2024 06:21:19 GMT  
		Size: 3.3 MB (3331627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6a2831f5616aee79afc6e04ec8fffa2b1118e24dc073576551b41e997cceda4`  
		Last Modified: Sat, 22 Jun 2024 06:21:18 GMT  
		Size: 20.0 KB (20003 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-jdk` - windows version 10.0.20348.2529; amd64

```console
$ docker pull openjdk@sha256:97bbeaf486f75fac06a11579c69d014ac639865e66561f182f1b198ed6de8a7c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2325282074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e58ef7bef4342f6bd6f6998564c85f0f7747d1af9a6a6d9f94060489933174`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 19 Jun 2024 19:58:05 GMT
RUN Install update 10.0.20348.2529
# Tue, 02 Jul 2024 00:57:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Jul 2024 00:59:00 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 02 Jul 2024 00:59:01 GMT
ENV JAVA_HOME=C:\openjdk-23
# Tue, 02 Jul 2024 00:59:07 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 02 Jul 2024 00:59:08 GMT
ENV JAVA_VERSION=23-ea+29
# Tue, 02 Jul 2024 00:59:08 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/29/GPL/openjdk-23-ea+29_windows-x64_bin.zip
# Tue, 02 Jul 2024 00:59:09 GMT
ENV JAVA_SHA256=58846b365aa5e7c3baedfba5852277c20d27949d25686685aee0c5b6896f7d77
# Tue, 02 Jul 2024 00:59:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 02 Jul 2024 00:59:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb373ec9afdfc5f09b9380d981e0c61f9c7b48537b887135c7c66810086e705e`  
		Last Modified: Fri, 21 Jun 2024 00:27:54 GMT  
		Size: 729.6 MB (729591500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:661bae3e8b139ee91ff9e5ba8c4ccc2fecfd87af85742f37fd0cb5c9e90b75fc`  
		Last Modified: Tue, 02 Jul 2024 00:59:51 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7126d8cd8aa60a7060a5568526a07525d93a1d1dce84966b3d7536fbadb98080`  
		Last Modified: Tue, 02 Jul 2024 00:59:51 GMT  
		Size: 361.0 KB (361023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e4b50af9b684c0641a5ca2b823a5c85babd22f54639a32b8e9d261e14e88e6b`  
		Last Modified: Tue, 02 Jul 2024 00:59:51 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e395a0357292328f20540709063ef60dbf5ef5e470ead3abc9d63af08de098`  
		Last Modified: Tue, 02 Jul 2024 00:59:51 GMT  
		Size: 311.7 KB (311692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b790a103ba1c2d6e5349a1e2980082ee4c3ab2f006c5f2753644808ddb437b`  
		Last Modified: Tue, 02 Jul 2024 00:59:49 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803085a80ed0a44874d39fda3035310e966772293b870e0f5582dd223b3c5793`  
		Last Modified: Tue, 02 Jul 2024 00:59:49 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df479fc37d68502e8b1abe3a368c681b945a5a102483569c69a8fe2bbde45c2d`  
		Last Modified: Tue, 02 Jul 2024 00:59:49 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6ed442f407e9a03a912dc2b072fb3bb7b6d1c0f21fddeda4487f002d65d477`  
		Last Modified: Tue, 02 Jul 2024 01:00:00 GMT  
		Size: 206.4 MB (206411161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5965835b3906efe41c0d0b54f78ad63ba10c96a8c34f12892d211709e4475018`  
		Last Modified: Tue, 02 Jul 2024 00:59:49 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:23-jdk` - windows version 10.0.17763.5936; amd64

```console
$ docker pull openjdk@sha256:6ad28fa40857623c5a106ba95dd758bb58cd7e6e073eea9fc8c1e63de6e79b18
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2427989654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e697e76e8bf8defa9ea349eb4a83f4b28fbbbdf32dc872c4084637a26a93d485`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Tue, 02 Jul 2024 00:57:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Jul 2024 00:58:30 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 02 Jul 2024 00:58:31 GMT
ENV JAVA_HOME=C:\openjdk-23
# Tue, 02 Jul 2024 00:58:53 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 02 Jul 2024 00:58:54 GMT
ENV JAVA_VERSION=23-ea+29
# Tue, 02 Jul 2024 00:58:54 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/29/GPL/openjdk-23-ea+29_windows-x64_bin.zip
# Tue, 02 Jul 2024 00:58:55 GMT
ENV JAVA_SHA256=58846b365aa5e7c3baedfba5852277c20d27949d25686685aee0c5b6896f7d77
# Tue, 02 Jul 2024 00:59:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 02 Jul 2024 00:59:40 GMT
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
	-	`sha256:fb977b62184d8883ac9d4e3daea6b282cfc1237e43a07cafe2a80bd49e9fe0bc`  
		Last Modified: Tue, 02 Jul 2024 00:59:45 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d33e4ce7a0b18cdba54559146c1b51b977526b82ce9d6015a7f453222a911d3`  
		Last Modified: Tue, 02 Jul 2024 00:59:45 GMT  
		Size: 500.0 KB (500013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac58816af801d4d5779bd93c716892bedb3e327d4c6479b7654c15d9627e63c9`  
		Last Modified: Tue, 02 Jul 2024 00:59:45 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788e89f0d25e172e7c8f7588378afa1b1702a72bed69af928f7914f6d2c86086`  
		Last Modified: Tue, 02 Jul 2024 00:59:45 GMT  
		Size: 354.3 KB (354342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9678d5d56a4981d3b6a7a59b8e2b43b9dbdcc55346f996267af68fc017369894`  
		Last Modified: Tue, 02 Jul 2024 00:59:44 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75a1af750c9d4771c7ec39f26952298dff166b249eff49cb4deda573bf4fdf3`  
		Last Modified: Tue, 02 Jul 2024 00:59:44 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:490583eaf4f3c4af56bfe469659a0d272ceb01b824700f52a9b1a1c14dd66db0`  
		Last Modified: Tue, 02 Jul 2024 00:59:44 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3164425146729a5047bf19e838e95bb69abd9ba99e8c169559d29ad0a1af38f`  
		Last Modified: Tue, 02 Jul 2024 00:59:54 GMT  
		Size: 206.4 MB (206446300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38059dea5b5967d3d244c444c3c02c7d0fdffa1e6200b496f9bfbc849881487e`  
		Last Modified: Tue, 02 Jul 2024 00:59:44 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
