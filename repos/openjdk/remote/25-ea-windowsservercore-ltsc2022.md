## `openjdk:25-ea-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:b710b217a96539a8ecc74a79a3d28681469ed090698fce381d21a1333c409ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `openjdk:25-ea-windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull openjdk@sha256:1fcdef628e17a3484212e562f28ee874fbad429a9bfc4a56284eeeb74d4a68e5
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2470882360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbab32008d48f89b4b481aadfca3a5e0b501f68bc876c77eac7ffc2c45a4475f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Fri, 31 Jan 2025 22:25:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Jan 2025 22:27:34 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 31 Jan 2025 22:27:36 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 31 Jan 2025 22:27:46 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 31 Jan 2025 22:27:47 GMT
ENV JAVA_VERSION=25-ea+8
# Fri, 31 Jan 2025 22:27:49 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/8/GPL/openjdk-25-ea+8_windows-x64_bin.zip
# Fri, 31 Jan 2025 22:27:51 GMT
ENV JAVA_SHA256=3ea9473d90c2a51f51d40081e60eb97a8fd26b8f787d9b44a51f102714942cf6
# Fri, 31 Jan 2025 22:28:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 31 Jan 2025 22:28:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71f85c9141db75f8fc9268ca5711e72eb0aebe7dd6a36abbe915f9a25b867dc`  
		Last Modified: Fri, 31 Jan 2025 22:28:30 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32886b9bccd03909abd9bd7f2c7b010cc032c3e467a0b3319146701d3bed0616`  
		Last Modified: Fri, 31 Jan 2025 22:28:30 GMT  
		Size: 365.1 KB (365134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:541de414409d9a1bd158da2596368f3c72494381e41649bb566c4e55037eba3f`  
		Last Modified: Fri, 31 Jan 2025 22:28:30 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc839431119e5c92250d8e32357cbcfef99ce1c7b88c92250bfe33f2711fd123`  
		Last Modified: Fri, 31 Jan 2025 22:28:30 GMT  
		Size: 312.7 KB (312670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:988ec8e38b236ebe94453749be3271c37c619673d48bc1ef9a9056bbcaafbbae`  
		Last Modified: Fri, 31 Jan 2025 22:28:28 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c72dc12907c4deb46f88646b3c29463b5cf71ae397f4da5e6ac1e2ee693d7fc`  
		Last Modified: Fri, 31 Jan 2025 22:28:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20d223b0839ab6e81252769c96f7871ecf1afc6ce090346386d43cc18db5b6a`  
		Last Modified: Fri, 31 Jan 2025 22:28:28 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7e9c483440fa0de44b91e2ae75d2060293b261072da56c4d7c22fc57d73e90`  
		Last Modified: Fri, 31 Jan 2025 22:28:39 GMT  
		Size: 207.8 MB (207811427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9ab527f8f9a73f9d3130ff650c66a3d9766cd151f167acebbf8504bf900347`  
		Last Modified: Fri, 31 Jan 2025 22:28:28 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
