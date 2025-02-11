## `openjdk:25-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:c33b4af3d0f3cdc82afaeb9ba50efeb0d8226babc260c098761029b001a8d2a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `openjdk:25-jdk-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull openjdk@sha256:f650c51434d86949e95dfcdb2e1ba26dd45bee63c70f7bd9661135be36f36b64
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2330761709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b15634b5d1bceb4fc9d47cf6decc9bb4a12d352bf6e9cb253c1e9b4453eccc1`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Tue, 11 Feb 2025 00:27:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Feb 2025 00:28:39 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 11 Feb 2025 00:28:39 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 11 Feb 2025 00:28:50 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 11 Feb 2025 00:28:51 GMT
ENV JAVA_VERSION=25-ea+9
# Tue, 11 Feb 2025 00:28:52 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/9/GPL/openjdk-25-ea+9_windows-x64_bin.zip
# Tue, 11 Feb 2025 00:28:52 GMT
ENV JAVA_SHA256=422ffa84afebca61d5ff96e0459231633ad47f082eb11fbecdb64c76e37b35ea
# Tue, 11 Feb 2025 00:29:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 11 Feb 2025 00:29:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d33258ab6e0502e72c64239e0dd5c590bf2a156c632b46d34c8127a39537053`  
		Last Modified: Tue, 11 Feb 2025 00:29:35 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31153d41017e64952ec3b550f20ddae4febdf7208e9c920eb50966f878ce8b4a`  
		Last Modified: Tue, 11 Feb 2025 00:29:35 GMT  
		Size: 353.9 KB (353902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d902c882c8a22b22919fb02bee9661449192ab8bcafc02a3deb447a8579855f7`  
		Last Modified: Tue, 11 Feb 2025 00:29:35 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82c1d9a7f8ffc141b71076daa2443eb2de53d6ae203846992c96ecc9337998f7`  
		Last Modified: Tue, 11 Feb 2025 00:29:35 GMT  
		Size: 338.3 KB (338343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18d69a662a2194044d3794bcac38bbf0cab7a1e380c515aaa5a5ba4755cc0932`  
		Last Modified: Tue, 11 Feb 2025 00:29:33 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1aec3a8d316b1c0b1671699bf88a707af5a877273e073bd5f44c2d390aa87a`  
		Last Modified: Tue, 11 Feb 2025 00:29:33 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0a46b2d5242b131507997b788234f375db8487fb01fade330ae6fbac38fddd`  
		Last Modified: Tue, 11 Feb 2025 00:29:33 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d98a337c23ed13506117abd3406da9b0627caf5b3d503d0806641b2304d541`  
		Last Modified: Tue, 11 Feb 2025 00:29:44 GMT  
		Size: 207.8 MB (207849350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dece062bf4bbdde052aec51e1c0265e371f08157140cb2846ca5bb6281714aa`  
		Last Modified: Tue, 11 Feb 2025 00:29:33 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
