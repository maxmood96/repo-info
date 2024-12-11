## `openjdk:25-ea-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:c469537e564ae3d3ee2e45823e68c29b7c03a4a4b814a6275854c31b67649143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `openjdk:25-ea-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull openjdk@sha256:0a63467848125bca5274592247ef7e1c95cf5d2ab6c5dbd23ba1427523885bb5
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2463487749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80f2188754b1e0422f5af20dccce1ba3f1523f79fa1492950705618337a6ddd6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:38:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:38:36 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:38:37 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 11 Dec 2024 20:38:43 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:38:44 GMT
ENV JAVA_VERSION=25-ea+1
# Wed, 11 Dec 2024 20:38:45 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/1/GPL/openjdk-25-ea+1_windows-x64_bin.zip
# Wed, 11 Dec 2024 20:38:45 GMT
ENV JAVA_SHA256=e613057ce9dd454d410ac2462a504dd7679eeec29d28c18c9d16c6d12f12f346
# Wed, 11 Dec 2024 20:39:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:39:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdec359a832a8d82911aeb2143d055348b4731f60f3a5bcccaf277e6fa615b63`  
		Last Modified: Wed, 11 Dec 2024 20:39:10 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e61c2db8678a0aa0bf5779a9ec2ffd0a3fe912d8d6419d1326a57af24f626445`  
		Last Modified: Wed, 11 Dec 2024 20:39:10 GMT  
		Size: 347.8 KB (347805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ba0e434436a5c3095e6d3946e0eabca53e22c0927ac3c610471f2f07f17b7c`  
		Last Modified: Wed, 11 Dec 2024 20:39:10 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d448958b6c1bbf218fc77e9cce540c300ca7e33becf5f56fb0c7379b2cae9302`  
		Last Modified: Wed, 11 Dec 2024 20:39:10 GMT  
		Size: 335.8 KB (335765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:937fa23c2b0ff82779549b13acac50d6f53b8361ccbf934ed234484a0a5e4ef7`  
		Last Modified: Wed, 11 Dec 2024 20:39:08 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28cd080ec18c2b5bf9cfd6a4acc9deb1071827bb06e237e4f44881196f70e7e`  
		Last Modified: Wed, 11 Dec 2024 20:39:08 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a56c0d52f5e936bede65619529e692eaf5ce2833a2622cddcbef55b7b59e729`  
		Last Modified: Wed, 11 Dec 2024 20:39:08 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:951f580c7ffdc27c38b602fc45ae0cabe61174d56610e24decd997754968791c`  
		Last Modified: Wed, 11 Dec 2024 20:39:22 GMT  
		Size: 208.9 MB (208922419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee60ff16f30dd150cd5f3d1955bf38767cfa3316ee2da00eedd7c310b6705f1f`  
		Last Modified: Wed, 11 Dec 2024 20:39:08 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
