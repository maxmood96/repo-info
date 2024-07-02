## `openjdk:23-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:9024ca12e4968ed252a95174fe178b5b452dd714793b842a3779033eeb07e1a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2529; amd64

### `openjdk:23-windowsservercore-ltsc2022` - windows version 10.0.20348.2529; amd64

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
