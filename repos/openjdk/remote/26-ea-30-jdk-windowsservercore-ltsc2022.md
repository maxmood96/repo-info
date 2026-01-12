## `openjdk:26-ea-30-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:9cda60c5be74ee21192ac8021b13423eac627f3f428073145bad3245ef0a9a37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `openjdk:26-ea-30-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull openjdk@sha256:73cf31b2cf237f1fb96036a9c42fa8fa03fb940d653db6802ff9dd0c811c8b44
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2004981479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aefe9620825fce3b506ae053437a3e99f57c3e6d21440a23c123fb01ed3571e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Mon, 12 Jan 2026 20:07:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 12 Jan 2026 20:08:05 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 12 Jan 2026 20:08:06 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 12 Jan 2026 20:08:13 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 12 Jan 2026 20:08:15 GMT
ENV JAVA_VERSION=26-ea+30
# Mon, 12 Jan 2026 20:08:16 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_windows-x64_bin.zip
# Mon, 12 Jan 2026 20:08:17 GMT
ENV JAVA_SHA256=43834141dc2e692e91f2f08c4cdfcbe91d8e33dea1abaace5b34ca7b14913f44
# Mon, 12 Jan 2026 20:09:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 12 Jan 2026 20:09:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ae91ebb6b06916422f2db8a3c6f63e9ad96d44267ea6c1205256cd05e31ad9`  
		Last Modified: Mon, 12 Jan 2026 20:21:42 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d05d2dbb94cd655893e275edfdc5a2e8865eb5e7e9e1dcece1cc5c60c612687`  
		Last Modified: Mon, 12 Jan 2026 20:21:42 GMT  
		Size: 504.0 KB (503972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a1f7c389edcc01cbf5f679e45114356f3de11118cfb7f73ef1a99d377007e2`  
		Last Modified: Mon, 12 Jan 2026 20:21:42 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a14bae3e2e3b2196d213bbbb02706c7efece708d5e200b074c97be22b209d9c`  
		Last Modified: Mon, 12 Jan 2026 20:21:42 GMT  
		Size: 351.3 KB (351326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de18327bf00e75dfb47f7bfca5ff124f96ee7c65f3a534977cc8252c64c813a7`  
		Last Modified: Mon, 12 Jan 2026 20:21:42 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e498bca2a15390ffddac3432ac1c189f099a15acc8b24610c3f73331268435`  
		Last Modified: Mon, 12 Jan 2026 20:21:43 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2b94618f57a7ee1523594dad08b526cdc8b93697ab9f11bd0cfd6d5254539e`  
		Last Modified: Mon, 12 Jan 2026 20:21:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15cdef37a5af2e7791ac6ec9f22b54d60ec6f1bdd33731c2469b676ce63a30ac`  
		Last Modified: Mon, 12 Jan 2026 20:21:49 GMT  
		Size: 224.2 MB (224239069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b798908a66396ae219748d4faaf06d6d490a80b5067e85c41c5ac9c2dcab2a0f`  
		Last Modified: Mon, 12 Jan 2026 20:21:43 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
