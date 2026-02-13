## `openjdk:26-rc-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:f333631ee8f1f69a5ea24b1b69891aadd6eacbccfd0fb0d460df4d5adf7b7c95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `openjdk:26-rc-windowsservercore-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull openjdk@sha256:89ccff92af910bc78d1d6f03ab0650d64629b77259f8f008f25a8d032f52fbaf
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2087749074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e907f4ee30e6981d8e178ead6938d3e237f51ed38b993c1d89fb905e09b0cbb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Fri, 13 Feb 2026 00:00:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 13 Feb 2026 00:01:29 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 13 Feb 2026 00:01:30 GMT
ENV JAVA_HOME=C:\openjdk-26
# Fri, 13 Feb 2026 00:01:39 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 13 Feb 2026 00:01:39 GMT
ENV JAVA_VERSION=26
# Fri, 13 Feb 2026 00:01:41 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/34/GPL/openjdk-26_windows-x64_bin.zip
# Fri, 13 Feb 2026 00:01:43 GMT
ENV JAVA_SHA256=a2dc3240208c735fe8107f27641987dd1283ad7e896d9aabaccb363fd93673ff
# Fri, 13 Feb 2026 00:03:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 13 Feb 2026 00:03:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4377001d10f5ca72eb3ce2d9d30ec1627a1afebcb2400f1a1e522c767f6b09a4`  
		Last Modified: Fri, 13 Feb 2026 00:03:15 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb6977528d81e5bf1ce2b6778aee1c4266bccf55eb80a45a1a7b039ebfec781`  
		Last Modified: Fri, 13 Feb 2026 00:03:15 GMT  
		Size: 492.0 KB (491986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c7ad26c16c9f4b71d61e9a04ae02a7b1175a11ee8949a42e6003fb6a802284`  
		Last Modified: Fri, 13 Feb 2026 00:03:15 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da08caee7025ad4a0754541e369c0d5cf2df831ec44cff42e81fa45e4cada5c3`  
		Last Modified: Fri, 13 Feb 2026 00:03:15 GMT  
		Size: 338.5 KB (338508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:300ec21561c646c37d384b255c0b585724f53401b901ca6b5f4ad6ee10a327e8`  
		Last Modified: Fri, 13 Feb 2026 00:03:13 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858f024b8646dc1973413753fb88e274ef33aba1bd715d4c6f7aa8d3d24abe6e`  
		Last Modified: Fri, 13 Feb 2026 00:03:13 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a6d36b5a7165a8ee6314f11aeefe86343f42d7bfce2d880047ba70b582a1a57`  
		Last Modified: Fri, 13 Feb 2026 00:03:13 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05872fb7133436a1aa39f3fee78fa417dab4cb4d9ddfa2742844cf812245856`  
		Last Modified: Fri, 13 Feb 2026 00:03:30 GMT  
		Size: 224.3 MB (224253567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e898e4b236de1cdd8724b35ad1e030211b655f63cc3fe8c285ecd7e12069d6a`  
		Last Modified: Fri, 13 Feb 2026 00:03:13 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
