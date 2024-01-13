## `openjdk:23-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:4918ca156b0adb0df8f2dff017a1ca79f51ad3db362476c49b190c2239d23db2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `openjdk:23-jdk-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull openjdk@sha256:6fdae11d5b344d9ad693990c058ac1cbdcdd2f50a8a825a202e614a5216d913e
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2268457667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fb1a5044bbc5e2a04a4d94ac08e3186051e21c9a77e121b8dfbbba36186249d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Sat, 13 Jan 2024 01:19:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 13 Jan 2024 01:21:05 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 13 Jan 2024 01:21:06 GMT
ENV JAVA_HOME=C:\openjdk-23
# Sat, 13 Jan 2024 01:21:26 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 13 Jan 2024 01:21:27 GMT
ENV JAVA_VERSION=23-ea+5
# Sat, 13 Jan 2024 01:21:27 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/5/GPL/openjdk-23-ea+5_windows-x64_bin.zip
# Sat, 13 Jan 2024 01:21:28 GMT
ENV JAVA_SHA256=b2bb5cc22adbca49cd0c94baec87d0a3fefa9c147b6407ac219e4fed98a099b8
# Sat, 13 Jan 2024 01:22:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 13 Jan 2024 01:22:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aef73f1b9d460d899dafbea2b87046935dece615d1aa92761e0f906b8079090c`  
		Last Modified: Sat, 13 Jan 2024 01:22:17 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6a81691f6b2299718c079b9e8c6369234ef6a37cfae11763e016dba3330c0e0`  
		Last Modified: Sat, 13 Jan 2024 01:22:17 GMT  
		Size: 489.6 KB (489646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b894884c336bec46f3872f51dbf07592f99c64f27c9dc493a2ad312a441f4ff`  
		Last Modified: Sat, 13 Jan 2024 01:22:17 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb5e738371cee60ef7f7b602759947237b50cab5a7d41fd42b70bc26a663633`  
		Last Modified: Sat, 13 Jan 2024 01:22:17 GMT  
		Size: 341.9 KB (341909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07846657a7caaebbb7e549399df110fd115e28a6aa859f72fa7a7d955228d72`  
		Last Modified: Sat, 13 Jan 2024 01:22:16 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d9feb7d98943f1a1bbc5edaafad0778179f0206062333f45c44052e43277cc`  
		Last Modified: Sat, 13 Jan 2024 01:22:16 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4010d0275f6a6f91d2d4fb9b8583f22d530930b26d0c25c4cc35da7f468aae`  
		Last Modified: Sat, 13 Jan 2024 01:22:16 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce9fb18d68fb66eab0a1c8514c92172ad3e9ea95e4833f60fd0b594efcb04b5a`  
		Last Modified: Sat, 13 Jan 2024 01:22:27 GMT  
		Size: 197.9 MB (197895474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f8e64fc16fb261f46edb254ae148b7ea9295ac23bda4e573387b04b62a2f49`  
		Last Modified: Sat, 13 Jan 2024 01:22:16 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
