## `openjdk:24-ea-33-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:12ce411aa5cf9311bfc84ec9d8691d35b8c80fd137016f3bca46d6ea10a91e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `openjdk:24-ea-33-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull openjdk@sha256:5f39302859514454de74c58a59dd6b69e32183474d0db31944b401129dbf7785
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2471990923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1e0fe671452a12f1b9880291d9c01131046fb52f85bd0ac895e35da52650a79`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Tue, 28 Jan 2025 23:27:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 28 Jan 2025 23:27:42 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 28 Jan 2025 23:27:43 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 28 Jan 2025 23:27:49 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 28 Jan 2025 23:27:50 GMT
ENV JAVA_VERSION=24-ea+33
# Tue, 28 Jan 2025 23:27:51 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/33/GPL/openjdk-24-ea+33_windows-x64_bin.zip
# Tue, 28 Jan 2025 23:27:52 GMT
ENV JAVA_SHA256=2c9091018c7bf3181421a86a3aabfe9ea9c375ed3720c8525be78fb54aa5516d
# Tue, 28 Jan 2025 23:28:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 28 Jan 2025 23:28:16 GMT
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
	-	`sha256:b84afefee940e125e0eb91a5a5f25ebd07c158a86f2498e3bfc024d86f5eb14f`  
		Last Modified: Tue, 28 Jan 2025 23:28:22 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab591e34a1b8dab1dcaf98777590a5d71c30297713e112f6c4323a808f01a97f`  
		Last Modified: Tue, 28 Jan 2025 23:28:22 GMT  
		Size: 369.6 KB (369577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847de08e0d4750ab9eb3dffa543474e0c29d0500dbff7ee22de038a4c870172d`  
		Last Modified: Tue, 28 Jan 2025 23:28:22 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e1bceb93f69a146deee834d93c90fd8d01bc4dd54f44443ea8587b336d25a7`  
		Last Modified: Tue, 28 Jan 2025 23:28:22 GMT  
		Size: 353.6 KB (353593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb56fac2c380d028cc1a5c4d76a0234c186ba05eea7fe677291a7adbedcfe8ea`  
		Last Modified: Tue, 28 Jan 2025 23:28:20 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b7b1fc37db9ba91e5effd2ebb41e3dba718a0ec70dd3fb450e0d88d933df16f`  
		Last Modified: Tue, 28 Jan 2025 23:28:20 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd612a9c14355fa5b7b20dbcd48e29d9f8e4b8510cab780429462cd8fe1e495`  
		Last Modified: Tue, 28 Jan 2025 23:28:20 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2779a63f8a307e5e64933527bd2eacd5f612c78d04304f38b88f9ef1d2870bb`  
		Last Modified: Tue, 28 Jan 2025 23:28:31 GMT  
		Size: 208.9 MB (208874726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2038d577f2148708b701f61b8904a5cfcaf6d28568da7bd03f9a265a512409`  
		Last Modified: Tue, 28 Jan 2025 23:28:20 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
