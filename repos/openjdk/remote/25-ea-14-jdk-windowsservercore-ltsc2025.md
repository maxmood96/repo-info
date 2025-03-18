## `openjdk:25-ea-14-jdk-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:d813645c3a620308a9cbf9febc32b66d3fc1ffe901b2415f883c9c67a8bcade5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `openjdk:25-ea-14-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull openjdk@sha256:c5144b6ea730ca344a430ae864f9f09e0f27aec3d31f54ea4d8963fab9d2177c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3117318277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4389ff7e2d04125ac8aa3906dc85447d31241edbd5294a77f9d2a9cfbd402d3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Mon, 17 Mar 2025 21:15:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 17 Mar 2025 21:15:31 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 17 Mar 2025 21:15:32 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 17 Mar 2025 21:15:38 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 17 Mar 2025 21:15:39 GMT
ENV JAVA_VERSION=25-ea+14
# Mon, 17 Mar 2025 21:15:39 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/14/GPL/openjdk-25-ea+14_windows-x64_bin.zip
# Mon, 17 Mar 2025 21:15:40 GMT
ENV JAVA_SHA256=4616b55a7c0d6b65d650a08986609158fbffcfed8fc5fa589e9f356898d735d0
# Mon, 17 Mar 2025 21:15:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 17 Mar 2025 21:16:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5fc1859cd7cbca3bb7a2cbcfd11c1a147b8396d7084f3ed75bd06f0bde8390e`  
		Last Modified: Mon, 17 Mar 2025 21:16:09 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:797f3cdd1cb14a320e37695414677de17b379d87e5fe21ad5a370380825af188`  
		Last Modified: Mon, 17 Mar 2025 21:16:10 GMT  
		Size: 396.2 KB (396165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a56ce755c07a814b5098d4810d5fd2acd6a76f6ad18b287b84e74b751f4ea4f6`  
		Last Modified: Mon, 17 Mar 2025 21:16:09 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9291d5ae2b14f441336980fba5496dd3175fe8b02c4cc1b89d76cd21ac3f0d11`  
		Last Modified: Mon, 17 Mar 2025 21:16:09 GMT  
		Size: 378.8 KB (378775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c53ad5970bcdcc780b072072e7a297cde1ba0375d5624f25be5f9269aa89d5`  
		Last Modified: Mon, 17 Mar 2025 21:16:08 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553c677e4f5901e48b2deba852ce22964898e3d67e586f7e139f31fa3ad35df6`  
		Last Modified: Mon, 17 Mar 2025 21:16:08 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6768ef7fe08d0e2a960f84ad570a08a98e237ef5c16555f1e044d193ca205e66`  
		Last Modified: Mon, 17 Mar 2025 21:16:08 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85f9cc630b55752189667ce14d6b4cfa081544f2be592fa69b7a1c40f555d3fa`  
		Last Modified: Mon, 17 Mar 2025 21:16:21 GMT  
		Size: 207.9 MB (207887798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f780d22cadffda04063ac4f5e4680577d6a7c99c257a8672b61ffc8f1809c628`  
		Last Modified: Mon, 17 Mar 2025 21:16:08 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
