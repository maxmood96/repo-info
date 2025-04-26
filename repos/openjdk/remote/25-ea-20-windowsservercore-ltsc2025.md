## `openjdk:25-ea-20-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:259f5effd626ca92a1d52eec0214f6b410cd4b1164e6a5731c42d6a2810428ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3781; amd64

### `openjdk:25-ea-20-windowsservercore-ltsc2025` - windows version 10.0.26100.3781; amd64

```console
$ docker pull openjdk@sha256:ac3ca599cefad714d36dbc05189ad61cb662351666bdcbe15d6cbc40267dcd2b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3604062240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:016d105a650f0aff167c9af5c86757558a65b0817598a0215be9e87367b3257d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Tue, 15 Apr 2025 10:03:37 GMT
RUN Install update 10.0.26100.3781
# Fri, 25 Apr 2025 21:50:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 25 Apr 2025 21:50:42 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 25 Apr 2025 21:50:43 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 25 Apr 2025 21:50:50 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 25 Apr 2025 21:50:51 GMT
ENV JAVA_VERSION=25-ea+20
# Fri, 25 Apr 2025 21:50:51 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/20/GPL/openjdk-25-ea+20_windows-x64_bin.zip
# Fri, 25 Apr 2025 21:50:52 GMT
ENV JAVA_SHA256=189b22f424bd7f7ef01de23f6e41fd183bc3b28da7db090dacba784054fe1f43
# Fri, 25 Apr 2025 21:51:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 25 Apr 2025 21:51:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a55b9bd12cfb5d81d64963683e6d5d0ba9423233c85140eff135128a64f7ee`  
		Last Modified: Fri, 18 Apr 2025 03:15:41 GMT  
		Size: 1.2 GB (1179854238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560f4f67a6412e5577071c0673b23d3d884e204c8ae8d79943638f9a45c357e2`  
		Last Modified: Fri, 25 Apr 2025 21:51:16 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b39ee62e7bcdbec8ded8f28c6e44b7ff06ca18c1579d0fefb0d1743a0b1869`  
		Last Modified: Fri, 25 Apr 2025 21:51:16 GMT  
		Size: 399.5 KB (399453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f476be7aec6524f25c899ce28b72b2068fd6046a9cfbc51c825668d98005b1c`  
		Last Modified: Fri, 25 Apr 2025 21:51:16 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6b08ae0f01699ca88c41b9c9d81a87077c39ad0545299011f505857e98080e`  
		Last Modified: Fri, 25 Apr 2025 21:51:16 GMT  
		Size: 377.7 KB (377695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fe98608ace7f170d309a8905898285b361bafb1d76caa482f59c54b51bd0e3`  
		Last Modified: Fri, 25 Apr 2025 21:51:15 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e62039adc6f994c2c08e82645854653db5ec9ab12c5b463432d4898a923057`  
		Last Modified: Fri, 25 Apr 2025 21:51:15 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de89a6e1873d07bd42c2290e916e5edf9f247395291fac21573bdd8168c9a87f`  
		Last Modified: Fri, 25 Apr 2025 21:51:15 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7409f835fa67ba43a6f2c8ed671d4fd7da4a9ad1ef4a0d07090f6b45bd457c5a`  
		Last Modified: Fri, 25 Apr 2025 21:51:35 GMT  
		Size: 208.1 MB (208115874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df49e8adeaa0a41f47ed954af5bb42417de2e93867aa0bb865d5b030d2e483e`  
		Last Modified: Fri, 25 Apr 2025 21:51:15 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
