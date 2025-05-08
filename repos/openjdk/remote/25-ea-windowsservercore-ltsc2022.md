## `openjdk:25-ea-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:f71ad884eddd701726c7c6a1023a5d385603b54b0ec45bd89c59beac8d79eda1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `openjdk:25-ea-windowsservercore-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull openjdk@sha256:397ca7e38b5b74a81757496212f1c65f26716627eab0d01300acd8a61d39c57f
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2483483728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63829a33fd7840bf71ba4f707ba69e91920a6c1052afa4631c9eabd6cd93d54b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Mon, 05 May 2025 17:29:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 05 May 2025 17:31:03 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 05 May 2025 17:31:04 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 05 May 2025 17:31:17 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 05 May 2025 17:31:18 GMT
ENV JAVA_VERSION=25-ea+21
# Mon, 05 May 2025 17:31:19 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/21/GPL/openjdk-25-ea+21_windows-x64_bin.zip
# Mon, 05 May 2025 17:31:20 GMT
ENV JAVA_SHA256=50dc1f432a184e23ec8364a00fb4a5f8f791d3eed3a4d36226a041d7de9047e0
# Mon, 05 May 2025 17:31:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 05 May 2025 17:31:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6ee194dfee460cc53e0f761b7ff976c08380d6cd1e70cc50ff92cfa99d176`  
		Last Modified: Thu, 08 May 2025 17:22:47 GMT  
		Size: 811.4 MB (811390127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77fe7ba8fcbeae3a54a422b9b8dbf0b9121bb120cf75d491227247c2eb7d58d6`  
		Last Modified: Mon, 05 May 2025 17:31:54 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3b13adf06acb720df564d4777bdda93c0ddb9521686cd8677870f3229c8135`  
		Last Modified: Mon, 05 May 2025 17:31:54 GMT  
		Size: 369.6 KB (369582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0996a0a18f83ff41e65217749193939342b4ea74d255b4a645d15065823a73a`  
		Last Modified: Mon, 05 May 2025 17:31:54 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0924f0a971e566d029767519052116c9c1b3ac4667631b105ce3c12b204a417`  
		Last Modified: Mon, 05 May 2025 17:31:54 GMT  
		Size: 320.7 KB (320679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d26788f68ea4c1ba446d6017ddbc2841a354849cce5f921f582c5ebe8082aebb`  
		Last Modified: Mon, 05 May 2025 17:31:52 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07a9b3d0c7d692bc4ca6b84a3cee100ac2aa34750fcb4cbf3c69fb25cb0b6dc`  
		Last Modified: Mon, 05 May 2025 17:31:52 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e2130f964c70ddd6cb327a0013e1ce68c04bae156f8273d04cbd93b59ee74b`  
		Last Modified: Mon, 05 May 2025 17:31:52 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde7b2a55a26ea1f5f1fa39b4a446354bb74d75e036f4f257a1e691c0f3c66f4`  
		Last Modified: Mon, 05 May 2025 17:32:03 GMT  
		Size: 209.2 MB (209203206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1760b30e3ff436378d8c3d843d51e580027d45e49ccdb3419f611873beed62da`  
		Last Modified: Mon, 05 May 2025 17:31:52 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
