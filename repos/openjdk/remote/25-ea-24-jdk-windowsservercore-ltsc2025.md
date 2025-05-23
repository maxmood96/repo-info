## `openjdk:25-ea-24-jdk-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:5e1e30917fc2546c5f66ad481a6236b06fc0e7b29d9082e38f8d92db6981f97c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `openjdk:25-ea-24-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.4061; amd64

```console
$ docker pull openjdk@sha256:b27edeae83ddc998a1515671c83f47cf27d64b68de4ada820211de7f90510f25
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3641335921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de3a5a412926df4cf04ca0b64a35a631a80872beb8273e28cd493f4bed515cb8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Fri, 23 May 2025 19:59:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 23 May 2025 20:00:08 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 23 May 2025 20:00:09 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 23 May 2025 20:00:16 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 23 May 2025 20:00:16 GMT
ENV JAVA_VERSION=25-ea+24
# Fri, 23 May 2025 20:00:17 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/24/GPL/openjdk-25-ea+24_windows-x64_bin.zip
# Fri, 23 May 2025 20:00:18 GMT
ENV JAVA_SHA256=2a8b2ea51b3b0b3751867a3117e7fde1235189e6d7601f5ffdb9b9160b270bf2
# Fri, 23 May 2025 20:00:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 23 May 2025 20:00:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Tue, 13 May 2025 21:56:34 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49fc0b84d26e30b055265d570016acc872eb918b3dc685633eb5a945ff5d9519`  
		Last Modified: Fri, 23 May 2025 20:00:50 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ced7210166d8ca282c967c19e06c9934eff0cd2026e9ecc9a48949f186ee895`  
		Last Modified: Fri, 23 May 2025 20:00:50 GMT  
		Size: 416.5 KB (416461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f96b6276c842ddf2c61166a92006f21cdcc78a0bea24970d01f99429d63dd134`  
		Last Modified: Fri, 23 May 2025 20:00:49 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7019a459234c72b2cda0ed941313b212746d64d8001e9fe31a7d41b41147195b`  
		Last Modified: Fri, 23 May 2025 20:00:50 GMT  
		Size: 394.0 KB (394048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e0ac3c903f146a6bd3ec678289e8bf469afaa097ef6cd1e89e6ead07918a22`  
		Last Modified: Fri, 23 May 2025 20:00:47 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78fb3c71952f2b6fed8b9cb1ae913e7e29b37dc28d932197f8af3bcd8220d3a`  
		Last Modified: Fri, 23 May 2025 20:00:47 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4eeebb7dc30d68005a19a9dd53f72704bade49df9b2322120a49d2f84edb7ca`  
		Last Modified: Fri, 23 May 2025 20:00:47 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9edf7a8fbd5addaf0731c0740a2c6126eaaf269fbc8a77f7e1bf778141d96bf3`  
		Last Modified: Fri, 23 May 2025 20:01:00 GMT  
		Size: 209.8 MB (209751822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd6042805c66aaa27ed75aa8e67be33547c142d9d226120442aef8dcf6bb412e`  
		Last Modified: Fri, 23 May 2025 20:00:47 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
