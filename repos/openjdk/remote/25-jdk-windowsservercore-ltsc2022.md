## `openjdk:25-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:def771bc49743a5d5c0490230c000c59d9785d396c1339e15dff87f361e1c239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `openjdk:25-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull openjdk@sha256:4b12849f0c08e9a332f06f0baff6f7368a4d74a5f27caeb9ec7be3280b8dc7fa
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2482294064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ff3c9739bb819c695f5aa2f5c219c4291522d61607bcaca59901c723b4b7ee4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Fri, 18 Apr 2025 18:45:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 18:46:09 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 18 Apr 2025 18:46:09 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 18 Apr 2025 18:46:15 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 18 Apr 2025 18:46:16 GMT
ENV JAVA_VERSION=25-ea+19
# Fri, 18 Apr 2025 18:46:16 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/19/GPL/openjdk-25-ea+19_windows-x64_bin.zip
# Fri, 18 Apr 2025 18:46:17 GMT
ENV JAVA_SHA256=29058ee51e7562ec5fb02d09a78c3540286db223bf48aacf93c4a95ed664fc7a
# Fri, 18 Apr 2025 18:46:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 18 Apr 2025 18:46:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6ee194dfee460cc53e0f761b7ff976c08380d6cd1e70cc50ff92cfa99d176`  
		Last Modified: Fri, 18 Apr 2025 03:14:44 GMT  
		Size: 811.4 MB (811390127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4885e6689ae6bfacdfc31859cb74ce202031e3d4646af124265ec30ce139fc6`  
		Last Modified: Fri, 18 Apr 2025 18:46:40 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127e166ba2fe15517d21e137ccda2a5e52a3bce409bf2bda9a7a7063a3c2b49f`  
		Last Modified: Fri, 18 Apr 2025 18:46:40 GMT  
		Size: 347.7 KB (347664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:933d89f8147b9e5b3a938c2aed65b6c2518d855427ab3fe318edc3d04bc35245`  
		Last Modified: Fri, 18 Apr 2025 18:46:40 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b7adbd3fc8d551c3a03fc1c9943dd64fe30012460704fdd99ed25357ebce22`  
		Last Modified: Fri, 18 Apr 2025 18:46:40 GMT  
		Size: 334.9 KB (334857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:641881ee4702fabe72d778d18f912873d686558dc2bd06a51ef3443ae4dd3898`  
		Last Modified: Fri, 18 Apr 2025 18:46:39 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc94ca20791e49c1761ae65e51614785b2689b6644cdd6236998e227778580f5`  
		Last Modified: Fri, 18 Apr 2025 18:46:39 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15d2be51cd75d85e58d19acde1fd9155745df8aced691acfcee2b9d5b7e33c9`  
		Last Modified: Fri, 18 Apr 2025 18:46:39 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826bd6d6d628178dffaae50cd651c2faa2f02138043fa391252428eb262754c8`  
		Last Modified: Fri, 18 Apr 2025 18:46:50 GMT  
		Size: 208.0 MB (208021281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a8abcdca6300544aa0c1c17f5d475d64a031b9a2f412307aa6388c149fb9d7`  
		Last Modified: Fri, 18 Apr 2025 18:46:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
