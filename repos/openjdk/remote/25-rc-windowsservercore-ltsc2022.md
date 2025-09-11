## `openjdk:25-rc-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:da20e2645fde828d13b7c9bd520429db8bde854736fa104880a8a21fb5019dae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `openjdk:25-rc-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull openjdk@sha256:0dac23c21e696b24d9ae5367f3d4f71fcffedf2c097926a54c26962d8bf9fefa
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2501761733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e0203b19549b75152d9ace564abd0e2475ba50b45e8490a8dbc2ce5b8c3b233`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 10 Sep 2025 21:49:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:58:55 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 10 Sep 2025 21:58:56 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 10 Sep 2025 21:59:02 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 10 Sep 2025 21:59:02 GMT
ENV JAVA_VERSION=25
# Wed, 10 Sep 2025 21:59:03 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/36/GPL/openjdk-25_windows-x64_bin.zip
# Wed, 10 Sep 2025 21:59:03 GMT
ENV JAVA_SHA256=85bcc178461e2cb3c549ab9ca9dfa73afd54c09a175d6510d0884071867137d3
# Wed, 10 Sep 2025 21:59:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 10 Sep 2025 21:59:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9811425449e84dcbd33b2ae7b7f37c3b7fd53dcd7b0401fd37de5fddd1a09096`  
		Last Modified: Wed, 10 Sep 2025 21:55:58 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e846c6dd3e143320da9b7961b894adca88516a63cf6882dab95406042615b89`  
		Last Modified: Wed, 10 Sep 2025 21:59:55 GMT  
		Size: 355.5 KB (355514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0877c7465661e9fe34ab7de4f50f268467906a0827d4d958c1e27cab6a4ea338`  
		Last Modified: Wed, 10 Sep 2025 21:59:55 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b19d989955aa33708d550def642f04fe1a82a7fdddb898fefd4f4498e434966`  
		Last Modified: Wed, 10 Sep 2025 21:59:55 GMT  
		Size: 336.6 KB (336569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b26f4cdc9dbf368aaee3ce2c6fe46b4f4263b91b53fbdb5fe81e9a8e7906b5`  
		Last Modified: Wed, 10 Sep 2025 21:59:55 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2376b15f09a2950134e05c435b5d81f3388a8bcb8b6f663f84a8914e81df6468`  
		Last Modified: Wed, 10 Sep 2025 21:59:55 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dcbf5a7b586d794fcd5c9e3b5c47077f64b879e814c71a8d49e88689df3b008`  
		Last Modified: Wed, 10 Sep 2025 21:59:55 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8e06451d295c0cde9c7f1054dee70deb4a36e2e2a027670089a319c6b9a3223`  
		Last Modified: Thu, 11 Sep 2025 00:23:58 GMT  
		Size: 218.9 MB (218916753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbce8fc7e92ed2a88218f3a58282e7d5f2c1c5ecb89f0dc8f964cef6d68e64a`  
		Last Modified: Wed, 10 Sep 2025 21:59:55 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
