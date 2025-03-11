## `openjdk:25-ea-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:009ee3562eab118f46a83b300171288dbc37d1d82aa68db9544de89c68864670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `openjdk:25-ea-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull openjdk@sha256:06f1af7fa770650d996a4db7a3248bc8a305cbe0ba2e8cb8f9d301671fee4a16
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2472376545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66195a042ee8e1372eab998dd67b800b2cf479edaf4a0c436a95aa34373d4d41`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Mon, 10 Mar 2025 21:05:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 10 Mar 2025 21:06:16 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 10 Mar 2025 21:06:17 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 10 Mar 2025 21:06:23 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 10 Mar 2025 21:06:24 GMT
ENV JAVA_VERSION=25-ea+13
# Mon, 10 Mar 2025 21:06:24 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/13/GPL/openjdk-25-ea+13_windows-x64_bin.zip
# Mon, 10 Mar 2025 21:06:25 GMT
ENV JAVA_SHA256=5182d7ac4519ceda5c809ccaa65ed9f2bea331524a65f59c3fccfe52fc878ac6
# Mon, 10 Mar 2025 21:06:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 10 Mar 2025 21:06:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a146723cf5b549f9d0d2fb3c7deb4fe3e62fd4ff402d1bfd5f00c5131e8946`  
		Last Modified: Mon, 10 Mar 2025 21:06:54 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d6eb97dd92925a9ff756f3b7f29e11e53f5aa2fecde4b0f37a2e2bda48e56b`  
		Last Modified: Mon, 10 Mar 2025 21:06:54 GMT  
		Size: 375.2 KB (375246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8c1aa1319d63eaf2e0cb7d6666ed7a40f8c59acc4635239dcbafb8cb7aa799`  
		Last Modified: Mon, 10 Mar 2025 21:06:54 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:886c98b89b7d1ba14700577876fbd6b3630c04a8ed3058050f2c7415d789b30e`  
		Last Modified: Mon, 10 Mar 2025 21:06:54 GMT  
		Size: 354.5 KB (354496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43a188f92f878b82a67f37f81b9a286e667a447d8f47ab5e12a8c8e5b0a22ca`  
		Last Modified: Mon, 10 Mar 2025 21:06:52 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87f293452a56c47beddc137a11113bd4bc062d842e95a26206ce2c321988ff4`  
		Last Modified: Mon, 10 Mar 2025 21:06:52 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa90467f6e12f9898cc1dd84e3c72fb9c3432b95e1b9f424f16854413e21c573`  
		Last Modified: Mon, 10 Mar 2025 21:06:52 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3fdb1ea33f83e9a903b0760d880ff9a603c1f5b4cece404d13fe84d495f2ef`  
		Last Modified: Mon, 10 Mar 2025 21:07:03 GMT  
		Size: 207.8 MB (207781086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41db02b87535953a5a8b73e31d77447ec91334b1c37835ae2c13d52b3b1cd7c`  
		Last Modified: Mon, 10 Mar 2025 21:06:52 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
