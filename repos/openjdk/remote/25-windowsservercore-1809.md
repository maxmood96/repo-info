## `openjdk:25-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:715b4b7045904bdb7f149778f9f2f246890a3f74e9fd998c35e5755a5dedc89c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `openjdk:25-windowsservercore-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull openjdk@sha256:7e75a816f9703e64b81ceef113f59414eb62e845ed4a47ae89d28bb409a3c6ef
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2402935581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd1770abae121b7e0ca5c204d26a49f2affdc466e33128170b0de810f740cc7`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Fri, 30 May 2025 17:45:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 30 May 2025 17:46:11 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 30 May 2025 17:46:11 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 30 May 2025 17:46:18 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 30 May 2025 17:46:18 GMT
ENV JAVA_VERSION=25-ea+25
# Fri, 30 May 2025 17:46:19 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/25/GPL/openjdk-25-ea+25_windows-x64_bin.zip
# Fri, 30 May 2025 17:46:19 GMT
ENV JAVA_SHA256=a6f3324a22501815f46fc9bd0a1e2e56d83dbad803e421c543644cb50539a8da
# Fri, 30 May 2025 17:46:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 30 May 2025 17:46:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95a939635fd6bec8c1562dcdbdde2fdb64095d1be9873313939c878db6f7279`  
		Last Modified: Tue, 13 May 2025 17:48:34 GMT  
		Size: 463.4 MB (463449115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a80224b5be860207c60e1d027571a8562cfc6abdaa4e12a27a565d4cba5dcf`  
		Last Modified: Fri, 30 May 2025 17:46:46 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a06d502e14825d0a7064405153b8eee327cfa22b4dca3c8355e5b351d345a9bf`  
		Last Modified: Fri, 30 May 2025 17:46:47 GMT  
		Size: 366.6 KB (366610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3dc38dbce4ed7fb131194a741d94b81e044a335ac9ca47b0febd1192f7458c1`  
		Last Modified: Fri, 30 May 2025 17:46:46 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ffac2a1ac15628ce950b20b184cc2464d03acb202d78527e446bfe91814d69`  
		Last Modified: Fri, 30 May 2025 17:46:46 GMT  
		Size: 343.2 KB (343228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96067c982388bb9af395ffa56ffe164e4486e5575bd2d901a645c65c50b9eeb7`  
		Last Modified: Fri, 30 May 2025 17:46:45 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf4ae265f49d063f363db11ba52e7564815f8ee9de2fd68c16caafd4ca00079c`  
		Last Modified: Fri, 30 May 2025 17:46:46 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd614c08be4215ecd3c4514571d312777f0e6c41ecef22f10e52fee34bb8cc02`  
		Last Modified: Fri, 30 May 2025 17:46:45 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1784f12ff548b83d5104cc65504ecce9a37a29870fd6fb50f60ff8c2ed12dcfb`  
		Last Modified: Fri, 30 May 2025 17:47:00 GMT  
		Size: 218.5 MB (218500522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee456ec6958348dde3d07afcddbc0c97233b36494b8ec930b8d6021f881298d7`  
		Last Modified: Fri, 30 May 2025 17:46:46 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
