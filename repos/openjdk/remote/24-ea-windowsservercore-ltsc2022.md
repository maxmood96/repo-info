## `openjdk:24-ea-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:e5345f496216dbbb4f2d63509d8c186911e7da5837423d100a1b8c1ade3070f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `openjdk:24-ea-windowsservercore-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull openjdk@sha256:3b01683944c9faf9854372290a2f5df0bee42f5dfefeddac72f17c96c3690bd1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1670934393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399bc1b8104564234b21f9d5bd1fc7b388a8f560e3b806871ae28bba21eac8a3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 20 Sep 2024 17:57:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 20 Sep 2024 17:59:39 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 20 Sep 2024 17:59:40 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 20 Sep 2024 17:59:47 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 20 Sep 2024 17:59:47 GMT
ENV JAVA_VERSION=24-ea+16
# Fri, 20 Sep 2024 17:59:48 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/16/GPL/openjdk-24-ea+16_windows-x64_bin.zip
# Fri, 20 Sep 2024 17:59:49 GMT
ENV JAVA_SHA256=842becbcc452ec5681e3bdc32d3aaa18634d97d24b9e5c3b49b221f30e9ceb0f
# Fri, 20 Sep 2024 18:00:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 20 Sep 2024 18:00:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4182a24ddc1b2db045c38ba97fa49bb45dfa37e50b0d7748612a76eb0e055c`  
		Last Modified: Fri, 20 Sep 2024 18:00:33 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6693489effcd55a92f194869a2c62c4a3c0e9b409038a1e6f925aeebfaf7e2`  
		Last Modified: Fri, 20 Sep 2024 18:00:33 GMT  
		Size: 373.0 KB (373001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42213b45badadc06aaaeb8196fd8580a4174241e5a71df71cf7a93c6173d435b`  
		Last Modified: Fri, 20 Sep 2024 18:00:33 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70787eeae62ae0fbe634f104b9384b03f7483cec018394fd1a4eedad3332886f`  
		Last Modified: Fri, 20 Sep 2024 18:00:33 GMT  
		Size: 321.4 KB (321438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb0701259e6f616ccd03ef65940a422d9c671d9fb4cbc3fd922d2bbf1a142ed`  
		Last Modified: Fri, 20 Sep 2024 18:00:32 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0253d3729ccf65aaf8bbf1b019d0972f64d5775fe59dcdc0a15ed07ad4e31389`  
		Last Modified: Fri, 20 Sep 2024 18:00:32 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7c5e1c9128db23dc0d1bd10fc52594af7f17f83d4fccdfde716986e7860ecf`  
		Last Modified: Fri, 20 Sep 2024 18:00:32 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53d1f5d5532a9189bf871147b1e356084d00242340e0d34b2635abd423e5bdb`  
		Last Modified: Fri, 20 Sep 2024 18:00:45 GMT  
		Size: 208.0 MB (208039591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a08a8ed3122cac418c86a72af40f30a632585ef190cf6353ebb32a91fb9caa`  
		Last Modified: Fri, 20 Sep 2024 18:00:32 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
