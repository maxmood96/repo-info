## `openjdk:22-ea-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:6ccadf757a585eec5cf94fdc4e1082ce4be1e879514b910232314a9c2daa3319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `openjdk:22-ea-windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull openjdk@sha256:b8a89e11b532aa456ebbecd21a7e5763614ea2ac313ebc36ff48e1922181e063
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2098817388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd6730a7f63a35c430b22338642dab2d9858316ec63809cbc9e33e70a516ed78`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Wed, 24 Jan 2024 20:49:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 24 Jan 2024 20:50:38 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 24 Jan 2024 20:50:40 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 24 Jan 2024 20:50:47 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 24 Jan 2024 20:50:48 GMT
ENV JAVA_VERSION=22-ea+32
# Wed, 24 Jan 2024 20:50:48 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/32/GPL/openjdk-22-ea+32_windows-x64_bin.zip
# Wed, 24 Jan 2024 20:50:49 GMT
ENV JAVA_SHA256=849804cc5a37d7768413d7e7a0e8088f31eb6ccc91b7f0fb7f517cefec0c5931
# Wed, 24 Jan 2024 20:51:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 24 Jan 2024 20:51:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a60a3bf6059b23da2b765b08c5e48ed008e261973de1b9b06945edb018889b3`  
		Last Modified: Wed, 24 Jan 2024 20:51:23 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e46f1722513bd3ae8d6d27b5e1d73f810d61870802cf66d224502f0a06fcf4d`  
		Last Modified: Wed, 24 Jan 2024 20:51:24 GMT  
		Size: 499.3 KB (499320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1881c7d9ea41f76d3d18442215a4990df630f03f45b90ce7103b7b7703971a`  
		Last Modified: Wed, 24 Jan 2024 20:51:23 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05954cc573a13fccd53b64bcb9c75b48ceda16619419aa12dc87910fe27ab915`  
		Last Modified: Wed, 24 Jan 2024 20:51:24 GMT  
		Size: 352.5 KB (352535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af6da6a76441e88df633453760c0c7d2120694569e5023d549555d19726d7e2`  
		Last Modified: Wed, 24 Jan 2024 20:51:21 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7262fd9b685bc5e2a3557524e71bc69a0ca8c2f7220adf9e09de5bc90c624ed1`  
		Last Modified: Wed, 24 Jan 2024 20:51:21 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7567affeb6ce5bd0d457bc5e32ee3c9b4cc43709ac88f8aa4c3acac2844a3de4`  
		Last Modified: Wed, 24 Jan 2024 20:51:21 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0911f607fcd78c11b70d026b2ca7f0476831018eaefbc1ce68dca623862c3eee`  
		Last Modified: Wed, 24 Jan 2024 20:51:31 GMT  
		Size: 197.7 MB (197744988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df26922996fea77472fc876aea71ef9026e680fe92daa8208efae788f6ac931`  
		Last Modified: Wed, 24 Jan 2024 20:51:21 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
