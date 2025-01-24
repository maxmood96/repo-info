## `openjdk:24-ea-32-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:62fa9e7b920fcb3d430610fcfefceb8cac63439761d43be79beeec9edf86b40b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `openjdk:24-ea-32-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull openjdk@sha256:30c49f275496565c03f96165c450159c8b33e9faa163fb214f88f063c5b2a487
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2471905571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d25f5b5a9a665d43e9b0bb2dec10b0c6d9ac747319783f3f5ff56c95d69f99`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Thu, 23 Jan 2025 22:26:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 22:27:18 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 23 Jan 2025 22:27:19 GMT
ENV JAVA_HOME=C:\openjdk-24
# Thu, 23 Jan 2025 22:27:26 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Thu, 23 Jan 2025 22:27:26 GMT
ENV JAVA_VERSION=24-ea+32
# Thu, 23 Jan 2025 22:27:27 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/32/GPL/openjdk-24-ea+32_windows-x64_bin.zip
# Thu, 23 Jan 2025 22:27:27 GMT
ENV JAVA_SHA256=e5f13b2b408e1c98310b5fac3025ff52a576a8ca77ad40ec8a1e90d8d1ca3094
# Thu, 23 Jan 2025 22:27:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 23 Jan 2025 22:27:56 GMT
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
	-	`sha256:67ea6003db03061d3996c029df04bb835460717c2dabb7bd287c115a17d3e8c5`  
		Last Modified: Thu, 23 Jan 2025 22:28:03 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf95d4f2bd025d92d79f37b2a178c04622f000efc7420ca79cef7498ac6c1d46`  
		Last Modified: Thu, 23 Jan 2025 22:28:03 GMT  
		Size: 363.8 KB (363775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4660a9e5ccae9aa2392986bed7cb60ec31cba0cda82aca9f1e9c368e23bee3b9`  
		Last Modified: Thu, 23 Jan 2025 22:28:03 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619b5659bba8b428e4054bb0872c141f46768cfff6d02e9ae06ad4fa05339ca8`  
		Last Modified: Thu, 23 Jan 2025 22:28:03 GMT  
		Size: 311.7 KB (311660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc40dbbcb3c467f890431a435df9803a643c1e08fb46c31a21884625c23222c`  
		Last Modified: Thu, 23 Jan 2025 22:28:01 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb4eacc5442b5cdd77d458d2a5a2d8cf0b8a186414f0e34735ae471567ce1d32`  
		Last Modified: Thu, 23 Jan 2025 22:28:01 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee524de7e1ddb8e06394cb972176922950cdb13007eeb5be95b83b002534a78`  
		Last Modified: Thu, 23 Jan 2025 22:28:01 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d56599663954a41f18cffefff7544d586e111524f76c06d77736730c80d4f0`  
		Last Modified: Thu, 23 Jan 2025 22:28:12 GMT  
		Size: 208.8 MB (208836797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50758e849d2ea3ed166b768c3da16c07ee6ef79a9030e18daab4e66c70849dc`  
		Last Modified: Thu, 23 Jan 2025 22:28:01 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
