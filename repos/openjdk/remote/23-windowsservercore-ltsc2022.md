## `openjdk:23-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:d34fd4a482811946b784bf58510d8e18e5026b7f9fa1773894c40692bfbee6c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2527; amd64

### `openjdk:23-windowsservercore-ltsc2022` - windows version 10.0.20348.2527; amd64

```console
$ docker pull openjdk@sha256:d2b5186764fe81ab1f111a2e7bb245c49de9e761a77e6285c8f5b5d36fa81535
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2325266334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:affceefdb2dac0b8eb134f7490d161c6725f09a1ecb8e36419331059e9510b54`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 07 Jun 2024 09:02:12 GMT
RUN Install update 10.0.20348.2527
# Fri, 14 Jun 2024 01:09:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Jun 2024 01:10:01 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 14 Jun 2024 01:10:01 GMT
ENV JAVA_HOME=C:\openjdk-23
# Fri, 14 Jun 2024 01:10:07 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 14 Jun 2024 01:10:08 GMT
ENV JAVA_VERSION=23-ea+27
# Fri, 14 Jun 2024 01:10:09 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/27/GPL/openjdk-23-ea+27_windows-x64_bin.zip
# Fri, 14 Jun 2024 01:10:09 GMT
ENV JAVA_SHA256=32824da64e6c9cf88cd5a05fe443afcbbc809ef6d31125581adb03c42574a650
# Fri, 14 Jun 2024 01:10:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 14 Jun 2024 01:10:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedf08888525e83e4a050655b4ec0d81647e59a69f7007a560df774a656da9bb`  
		Last Modified: Tue, 11 Jun 2024 17:49:21 GMT  
		Size: 729.6 MB (729579921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c602416917334b1b40b1766f31085829719a6388656a1d647ea2abc00feb0923`  
		Last Modified: Fri, 14 Jun 2024 01:10:35 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1688348a3e4a03822ceb98e9a0853377789bdf282f0527de04d5e05727ac7d6`  
		Last Modified: Fri, 14 Jun 2024 01:10:35 GMT  
		Size: 347.5 KB (347537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:282e59be6e048da1db31b57488437b0346e07ad59211aea20e081f5498fe1f5f`  
		Last Modified: Fri, 14 Jun 2024 01:10:35 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309a6a6b1565679ef69e92e5a886363b229811c76b220f8e606f5e1c9bf2f0fa`  
		Last Modified: Fri, 14 Jun 2024 01:10:35 GMT  
		Size: 334.0 KB (333978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2df6141da2f39383f00d8b9baf4172b3d28cc0ae33698eb819172d33fb2fdff`  
		Last Modified: Fri, 14 Jun 2024 01:10:34 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ae121de8a6a0e1327114763b4c00334606a8e564d0ad11a4645a02ec9f35d5`  
		Last Modified: Fri, 14 Jun 2024 01:10:34 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b2e682f0596f41e088e58caed5589f9366ed36a0e9dc60016a90a4e340dd66`  
		Last Modified: Fri, 14 Jun 2024 01:10:34 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c96f85068b253d6c15a4f7cbd5ad8f22dea552cb1f20f589fead4d183e4573`  
		Last Modified: Fri, 14 Jun 2024 01:10:45 GMT  
		Size: 206.4 MB (206398400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d9e97f45f32f989075295d437e83990377953e9ffcc4fe00c1203c7d84ca61`  
		Last Modified: Fri, 14 Jun 2024 01:10:34 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
