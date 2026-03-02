## `openjdk:27-ea-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:b204998431975bacef4163f442be100c755a6bc07791e3161c516db30ac3a5d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32370; amd64

### `openjdk:27-ea-windowsservercore-ltsc2025` - windows version 10.0.26100.32370; amd64

```console
$ docker pull openjdk@sha256:4bf38219511dbad7c38f385eff794d308e546e2c15158d312ad1d3a9b262ca01
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2190218926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:615d63b0adfa8e8f61d264170ded11f0007ca585f13fccb12329349e7d22c6c6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Feb 2026 22:21:49 GMT
RUN Install update 10.0.26100.32370
# Mon, 02 Mar 2026 21:25:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 02 Mar 2026 21:26:14 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 02 Mar 2026 21:26:15 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 02 Mar 2026 21:26:21 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 02 Mar 2026 21:26:21 GMT
ENV JAVA_VERSION=27-ea+11
# Mon, 02 Mar 2026 21:26:22 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/11/GPL/openjdk-27-ea+11_windows-x64_bin.zip
# Mon, 02 Mar 2026 21:26:23 GMT
ENV JAVA_SHA256=1ddea09bd3dbc807656ba83c0c62c5c0853849c254ca1d8b04786f58bc8d2341
# Mon, 02 Mar 2026 21:26:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 02 Mar 2026 21:26:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456534216d0c12d9314cda831989d54bb3f542d7d43d9772ba40654db6dbd7bc`  
		Last Modified: Tue, 10 Feb 2026 18:52:01 GMT  
		Size: 441.7 MB (441700471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85218dcf86c9e2514eedc07715218d85e9ed6365d1643d3444e2758598250d6b`  
		Last Modified: Mon, 02 Mar 2026 21:26:56 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e103e013778cbf5e33317ff88baa8b5893736880345e505e9887d81469e313`  
		Last Modified: Mon, 02 Mar 2026 21:26:56 GMT  
		Size: 371.7 KB (371712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12f387b8fb26c147bba9d2d81029538d40d597732bf175e2c3276fadfd3e633`  
		Last Modified: Mon, 02 Mar 2026 21:26:56 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec3e8e48eb799b4e5f7596f8b161adcb3d77caa8706a2d1db57146725d601ba7`  
		Last Modified: Mon, 02 Mar 2026 21:26:56 GMT  
		Size: 355.2 KB (355151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7661f27deb07e52f217d2ffa75645b063755a95ac893f86c3aa548ba3c3b39be`  
		Last Modified: Mon, 02 Mar 2026 21:26:55 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27019e83f7d26a4f955f9822b73e28f39e9cae2011c659a5f7a0f721ec9d00c`  
		Last Modified: Mon, 02 Mar 2026 21:26:55 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40bbb0e16b596f7fb33fabfa73710ecdd42409ca10cda9e544a6adc7fddb701f`  
		Last Modified: Mon, 02 Mar 2026 21:26:54 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc9b052aacd88779658d72d8ab5735538537b4bba42e193ef262cde25b214831`  
		Last Modified: Mon, 02 Mar 2026 21:27:11 GMT  
		Size: 224.7 MB (224724299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d70d9025517590aeee02024377ff2bc46d342fcebfeea05a60714a54fcf735a`  
		Last Modified: Mon, 02 Mar 2026 21:26:55 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
