## `openjdk:25-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:d6827a39fa6df62078e57279b05e935d2944500b2e04096d9ab4d47f52160c52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `openjdk:25-windowsservercore-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull openjdk@sha256:2dd778463a093faef7e0c677f71fbea2b32e2c3e4445b444a46917122ea312b7
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3718490239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c1b2e9281a353004c21c5ddf925bb2238dac3f0ff8d8942a1aa76108aae23b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Tue, 12 Aug 2025 20:34:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:34:32 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 12 Aug 2025 20:34:33 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 12 Aug 2025 20:34:38 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 12 Aug 2025 20:34:38 GMT
ENV JAVA_VERSION=25
# Tue, 12 Aug 2025 20:34:39 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/35/GPL/openjdk-25_windows-x64_bin.zip
# Tue, 12 Aug 2025 20:34:39 GMT
ENV JAVA_SHA256=1bf872a4dc38579963ad34a757b3077296c2d2ccfeeff041d1741a87e6bde898
# Tue, 12 Aug 2025 20:35:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 12 Aug 2025 20:35:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9426ac85c32ef0ad96af672f710cb3b41cb0cbf264db70747e3408a9b17c6149`  
		Last Modified: Tue, 12 Aug 2025 20:38:40 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09540fcd91088f65aa2a7120dcd96aa22f6ca0c5efbf17799e13a8a61c0fb37`  
		Last Modified: Tue, 12 Aug 2025 20:38:42 GMT  
		Size: 368.3 KB (368274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8362291cec62306fa7727b47e26d887dccdc103282470498cabde4d6f91adfdc`  
		Last Modified: Tue, 12 Aug 2025 20:38:41 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e03dd2ecbccdb43db22f0a5c5cad3062682413bad6fc00430c30462c6e3fcb7`  
		Last Modified: Tue, 12 Aug 2025 20:38:42 GMT  
		Size: 354.0 KB (353976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a87cbc2e8285567edb90fff4cede6f60f838c01e0fcae28e9c78b4ab0309c96`  
		Last Modified: Tue, 12 Aug 2025 20:38:42 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0609bbbda2633bec90b336a0b90b1f9ab8da7e1aca76b3f30f6254b9de8f0e3f`  
		Last Modified: Tue, 12 Aug 2025 20:38:37 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67f6cdfd6df9033c234b82fe75e36f1279fd8f1d8a6c1ea07550fba420fe7e43`  
		Last Modified: Tue, 12 Aug 2025 20:38:38 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40da4f1d72bbfaa765797d7df12fec22904584eaaced9ef4e3ebc9dd6804bb12`  
		Last Modified: Tue, 12 Aug 2025 20:47:01 GMT  
		Size: 218.9 MB (218929649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a8c7d540e59ceed9a8cfec7be93884be82f183a353f0e83166e730d483f93a`  
		Last Modified: Tue, 12 Aug 2025 20:38:38 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
