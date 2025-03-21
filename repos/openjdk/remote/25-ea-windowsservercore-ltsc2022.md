## `openjdk:25-ea-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:e205270c8c2225a90c9b2047f0822b270c11d7b014a7cb3216e8538cd27a8c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `openjdk:25-ea-windowsservercore-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull openjdk@sha256:7fffa5ae2d585664f5a9315639ed4b5f167dc2207c747ffd52009b90ee1b055d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2478547769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf45bb111caed9cd7ddf9ed3fe1a016463d07dec7b15c490703d598d4caf18b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Fri, 21 Mar 2025 17:21:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 21 Mar 2025 17:21:27 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 21 Mar 2025 17:21:28 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 21 Mar 2025 17:21:33 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 21 Mar 2025 17:21:34 GMT
ENV JAVA_VERSION=25-ea+15
# Fri, 21 Mar 2025 17:21:34 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/15/GPL/openjdk-25-ea+15_windows-x64_bin.zip
# Fri, 21 Mar 2025 17:21:35 GMT
ENV JAVA_SHA256=a095e71a2552995360224643760900b2c44fc91dad10cab9d289bed71fa936dc
# Fri, 21 Mar 2025 17:21:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 21 Mar 2025 17:21:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f379f06fa75c4e44e374efb896cc1a2a305a0ec35e4b5381c3a3d3f40b6b762f`  
		Last Modified: Fri, 21 Mar 2025 17:22:02 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8769919e37c5f16ced3587f18562a353374956be3ad123c666fc3c1c1ee375`  
		Last Modified: Fri, 21 Mar 2025 17:22:02 GMT  
		Size: 361.7 KB (361748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db36bd2a1f0f65ae5d121a12f57cc94469632ca277b9ffa9d2b9815b2ff97f9`  
		Last Modified: Fri, 21 Mar 2025 17:22:02 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209cc8b876cfd7786dbed6cadbffd064cd7f4129d29f78bc84f33a8d2117df9e`  
		Last Modified: Fri, 21 Mar 2025 17:22:02 GMT  
		Size: 347.5 KB (347533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e4e6f5024b44a5715e0171b91af8c8c7f8ba72a3173ab6a9e362e9a92390856`  
		Last Modified: Fri, 21 Mar 2025 17:22:00 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36803b8cbf1bfa57586e698b16ebf22ee0cf7b7897f2683a053ab3fe4982a7c7`  
		Last Modified: Fri, 21 Mar 2025 17:22:00 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275269dc2b115c47cfcb04c02fff89caac64a77bca3b7b3f1db8d77571f0e025`  
		Last Modified: Fri, 21 Mar 2025 17:22:00 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac8778d4970ae0eeb63f9d47f85215932aeebe93c60b66b03700e67bc8aa01e`  
		Last Modified: Fri, 21 Mar 2025 17:22:11 GMT  
		Size: 207.9 MB (207889484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9673b9c96cad644cb789913b5a1cd5ae085619aab32a641d886fe6b093e5db`  
		Last Modified: Fri, 21 Mar 2025 17:22:00 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
