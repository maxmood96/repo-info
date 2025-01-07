## `openjdk:24-ea-30-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:dda18ce0d81f5268b282454ed7608aa6546b1597b1a5920b1c453626f444d01a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `openjdk:24-ea-30-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull openjdk@sha256:664fe21f0bda4e53f955a98d61a422fecb2bcbf598b8b02a08390f45520d8955
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2463421658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f50f391966c9a52fda8b952da1a373b0e722540b2450163b173e4f1d9025634f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Mon, 06 Jan 2025 22:06:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 06 Jan 2025 22:07:00 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 06 Jan 2025 22:07:00 GMT
ENV JAVA_HOME=C:\openjdk-24
# Mon, 06 Jan 2025 22:07:07 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 06 Jan 2025 22:07:08 GMT
ENV JAVA_VERSION=24-ea+30
# Mon, 06 Jan 2025 22:07:08 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/30/GPL/openjdk-24-ea+30_windows-x64_bin.zip
# Mon, 06 Jan 2025 22:07:09 GMT
ENV JAVA_SHA256=d71df74a22fe12237dff1469d7adae9469331d0c68bbb3dc7145af17fd85cc76
# Mon, 06 Jan 2025 22:07:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 06 Jan 2025 22:07:36 GMT
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
	-	`sha256:b5da787373e799d1f3cab1cdf85af590d5d63ba85767b4c100e2e2a6c39c251c`  
		Last Modified: Mon, 06 Jan 2025 22:07:43 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5848ca1657704a01cd23d79c93bac681fe9b80b3adf2632808a90031bb0a3d29`  
		Last Modified: Mon, 06 Jan 2025 22:07:43 GMT  
		Size: 352.8 KB (352766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf88e41ea70a7a46c9e3e62b0232be091e976e63c4131c72747c9f07e7691eb`  
		Last Modified: Mon, 06 Jan 2025 22:07:43 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c6669e2281270caecebe0891ed98ba68f52cfcada1d98ae5a8d6d1449f8671`  
		Size: 339.4 KB (339368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dca2a37a5866146f091a583e456cc671635de2db28d3fbaede8c42b576f6079`  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9451359a5f8fe4d3d6d73e6d537314e70faa0399658093a9b0faf13afb34b9d`  
		Last Modified: Mon, 06 Jan 2025 22:07:41 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46fe1de17487b175b0dc666f2f3ab53bc8f776a0af778b5436e838f5352c548`  
		Last Modified: Mon, 06 Jan 2025 22:07:41 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279d751c11ebb100495914101f776a93df3ee0c1c5116fc8539a84d063ad6dba`  
		Last Modified: Mon, 06 Jan 2025 22:07:52 GMT  
		Size: 208.8 MB (208848205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d99f63891123d6b2dd0e9d68bb081eed83f17a2187fd2f54f09ce778428ad63`  
		Last Modified: Mon, 06 Jan 2025 22:07:41 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
