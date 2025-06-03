## `openjdk:25-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:9e966449d5f90f58ddf46a397008982d1d304d399c10af76e7a370ec921f745b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `openjdk:25-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull openjdk@sha256:d86fc760702bf52f1ea4b5ad5c40311a1188ee0a7e3c86df8e4559925f60fb7f
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2492812027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0538d599b829673ceda5c5222b3563ec1168f44a83b566688a8de1c7a880edbd`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Fri, 30 May 2025 17:37:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 30 May 2025 17:39:06 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 30 May 2025 17:39:07 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 30 May 2025 17:39:17 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 30 May 2025 17:39:18 GMT
ENV JAVA_VERSION=25-ea+25
# Fri, 30 May 2025 17:39:19 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/25/GPL/openjdk-25-ea+25_windows-x64_bin.zip
# Fri, 30 May 2025 17:39:19 GMT
ENV JAVA_SHA256=a6f3324a22501815f46fc9bd0a1e2e56d83dbad803e421c543644cb50539a8da
# Fri, 30 May 2025 17:39:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 30 May 2025 17:39:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af31692317cb98b95aeb69eaab4946b00f4b08ed0c90ef4bdb95f6bf4e8655e`  
		Last Modified: Fri, 30 May 2025 17:39:52 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f7b67e86a2555f11e2e0ff30aa977da0d5c389789ead22765cf1bc669fa0a2`  
		Last Modified: Fri, 30 May 2025 17:39:52 GMT  
		Size: 370.6 KB (370553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee45a8cd337c47a90f9e3e65db030640d4d57eae1725af0998ebaa61d7a40bd6`  
		Last Modified: Fri, 30 May 2025 17:39:52 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2cb574c8315bcc86a40f92cd6f6d068ba47ac6afd65824b3d943d972e2bfaab`  
		Last Modified: Fri, 30 May 2025 17:39:52 GMT  
		Size: 322.4 KB (322418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c81f616499897add6d15a222c7013fa1431d336742b89b7c17f364a4b7d35f3`  
		Last Modified: Fri, 30 May 2025 17:39:51 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c41e1211b898e024d93844e69fbb973c655e2d6ce5e658e010670d04e22d99`  
		Last Modified: Fri, 30 May 2025 17:39:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df62d9a58f28c4b83ebe58a7f9eded9ed23e387ee38bf32513f7eb6fdabd0a05`  
		Last Modified: Fri, 30 May 2025 17:39:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2484c2c5fa845fb5d0b9d531211a3c3c539b0d981aeae3492766424013a1e7f`  
		Last Modified: Fri, 30 May 2025 17:40:03 GMT  
		Size: 218.5 MB (218483120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d31265acdc3e2d81dd4c572848cfb8a3085aad9ec70efea1b2a2181b4aae16b`  
		Last Modified: Fri, 30 May 2025 17:39:51 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
