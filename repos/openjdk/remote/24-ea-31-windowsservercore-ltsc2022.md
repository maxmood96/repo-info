## `openjdk:24-ea-31-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:a10ff847a5ef1d1ae57de01119ef8006ac68ee12c422c4f1fdc3acea42a2b587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `openjdk:24-ea-31-windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull openjdk@sha256:b9c95bf6321affaa36d9afa505e9726455f46193a289dc409fe5b5ec9d935aa9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2471931050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce0435d3d3738be5128defcb30b3992792dbe0bcd31b4918cc1181ecd7f36e0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Tue, 14 Jan 2025 23:37:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:37:36 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:37:37 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 14 Jan 2025 23:37:42 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:37:42 GMT
ENV JAVA_VERSION=24-ea+31
# Tue, 14 Jan 2025 23:37:43 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/31/GPL/openjdk-24-ea+31_windows-x64_bin.zip
# Tue, 14 Jan 2025 23:37:43 GMT
ENV JAVA_SHA256=72536bad2fa20c7ead0367944940a684a359e43649870d3cdbccd46bcc3b4009
# Tue, 14 Jan 2025 23:38:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:38:02 GMT
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
	-	`sha256:7da954ca904eb925ca2c1399d3914db57c138133242c2338863e7e5946300c25`  
		Last Modified: Tue, 14 Jan 2025 23:38:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ad67c317d55d748daead122964a38ecf07c3976fc899cb0dc2f5f29b66321a`  
		Last Modified: Tue, 14 Jan 2025 23:38:09 GMT  
		Size: 360.8 KB (360788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a3ae78e5e579474d64c094b6d2a9a1b4e59f5d48a3eb1379c8783c4d4c9056f`  
		Last Modified: Tue, 14 Jan 2025 23:38:08 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94da7a3f45345b654966ad6d0f0ca7181ae4e27e54608b9b5878ee807fa5c9e2`  
		Last Modified: Tue, 14 Jan 2025 23:38:09 GMT  
		Size: 344.4 KB (344380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f650ccc353f60f41de872d8abc0b04fd6ec6ae68893886b2add558637a3f1c21`  
		Last Modified: Tue, 14 Jan 2025 23:38:07 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1099a3c234d1188056953e97f774df1de3632803e5cbcb84634815a56ccd357`  
		Last Modified: Tue, 14 Jan 2025 23:38:06 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e2546f1ccef89d7572bd6b9f928c74c2f0d71db3b1eac37bc8bb064a4c3f79`  
		Last Modified: Tue, 14 Jan 2025 23:38:06 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6fb71ed0588cc6fd2e3d8b002031c0b098b89a58ea555e206e54e43e61eaa9`  
		Last Modified: Tue, 14 Jan 2025 23:38:18 GMT  
		Size: 208.8 MB (208832901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e758ecaad71f9c6b8d9fb3f1079a2dd3f48227a6fe76d152b3028050c7a2335`  
		Last Modified: Tue, 14 Jan 2025 23:38:06 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
