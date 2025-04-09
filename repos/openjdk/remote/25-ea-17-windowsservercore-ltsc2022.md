## `openjdk:25-ea-17-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:a3e2e18a12a882fa5f9f09c36efb37fd05bc5c5e9ea5109b275afe23930c5ac8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3453; amd64

### `openjdk:25-ea-17-windowsservercore-ltsc2022` - windows version 10.0.20348.3453; amd64

```console
$ docker pull openjdk@sha256:c0954461eecf4d7baa4c6457e85240af50b08dc21963605f5d1b7dea659a3e6b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2479996220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e24d8c12f2378caf782056cdeb2c17e8170eb2fdc99de0fee3d41511f950d6c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 04 Apr 2025 23:10:04 GMT
RUN Install update 10.0.20348.3453
# Wed, 09 Apr 2025 00:48:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:48:38 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 09 Apr 2025 00:48:39 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 09 Apr 2025 00:48:44 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 09 Apr 2025 00:48:45 GMT
ENV JAVA_VERSION=25-ea+17
# Wed, 09 Apr 2025 00:48:45 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/17/GPL/openjdk-25-ea+17_windows-x64_bin.zip
# Wed, 09 Apr 2025 00:48:46 GMT
ENV JAVA_SHA256=46c47281310039b4e8d7e583a1629bfb2ca08a102794c3a68d1f2051101e9f5b
# Wed, 09 Apr 2025 00:49:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 09 Apr 2025 00:49:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510f1abe0ffe1466f946291b3ac20345b4a5e2063a896736990eae81bbf4bdb4`  
		Last Modified: Tue, 08 Apr 2025 21:40:38 GMT  
		Size: 808.8 MB (808803243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1725b949f271948738dd74be509c3f9885faee7889f91e60cb776d644e80093`  
		Last Modified: Wed, 09 Apr 2025 00:49:13 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc96e579503c81e09d425e008f32a85d6f65083661c993e9d875712df18c9791`  
		Last Modified: Wed, 09 Apr 2025 00:49:13 GMT  
		Size: 348.7 KB (348708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe17892597c242561d3c862d619654905e9dadfb73fc2a10b8e5b8936061a35`  
		Last Modified: Wed, 09 Apr 2025 00:49:13 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364e7f4c5f62ccf2d5c8c347977b5bdf977a3aac01859c4721272f42b4eab083`  
		Last Modified: Wed, 09 Apr 2025 00:49:13 GMT  
		Size: 335.1 KB (335053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec550b18eddc6bba47031c6916be9e4e60419e43275e992ac38cab644f9a1800`  
		Last Modified: Wed, 09 Apr 2025 00:49:10 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b317ba8e78c1b63d7773b3930df3ffa685441ea6ecc3c14a1d031b6fdc262fd2`  
		Last Modified: Wed, 09 Apr 2025 00:49:10 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a2fbed936c9dd0687cbe3834a2e426a4e6212aba8381077f85a41038fd95c3`  
		Last Modified: Wed, 09 Apr 2025 00:49:10 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19cdfe45a7631746d14a9334343ab1e59198d35a8d713cd07afeea0d410838cf`  
		Last Modified: Wed, 09 Apr 2025 00:49:22 GMT  
		Size: 208.3 MB (208308976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00972856ccc41326779514c3c03b345ba39103ee142dc5c62608f8b3fc576197`  
		Last Modified: Wed, 09 Apr 2025 00:49:10 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
