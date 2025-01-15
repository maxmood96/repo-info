## `openjdk:24-ea-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:a63ce3fcffd8c3efc242e5d0dcbc68a771a70a5f94bbb72d34a0ecb9334b99fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `openjdk:24-ea-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull openjdk@sha256:7943054362fbdf0f0cd24a687b3bfcd2695d4d1c016aade376c8077f79d2b990
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2331653020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:616c4a0375872db2f9f57fb83d2e189aaf2f66878b1a9805fb4acac5d53bffac`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Tue, 14 Jan 2025 23:43:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:44:22 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:44:22 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 14 Jan 2025 23:44:28 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:44:29 GMT
ENV JAVA_VERSION=24-ea+31
# Tue, 14 Jan 2025 23:44:29 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/31/GPL/openjdk-24-ea+31_windows-x64_bin.zip
# Tue, 14 Jan 2025 23:44:30 GMT
ENV JAVA_SHA256=72536bad2fa20c7ead0367944940a684a359e43649870d3cdbccd46bcc3b4009
# Tue, 14 Jan 2025 23:44:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:44:55 GMT
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
	-	`sha256:f5749b6a6e8ad8b0595ce97d114cbb758f1e990ee62fb8d672ed73419bf8236a`  
		Last Modified: Tue, 14 Jan 2025 23:45:02 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd1c2782b639d1e6e04a2142aec07d41d6d7911761aca21b00f26e0ecc17528a`  
		Last Modified: Tue, 14 Jan 2025 23:45:02 GMT  
		Size: 320.3 KB (320330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08ec5810411e41809bc941204fb1623b1e19624c3ca85406b9412cd01648ff33`  
		Last Modified: Tue, 14 Jan 2025 23:45:02 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072cd8bcd60d21fb6b88936828a2be1bee36617b0d6d744156aa2e6c65f492f1`  
		Last Modified: Tue, 14 Jan 2025 23:45:02 GMT  
		Size: 305.5 KB (305537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:835a281bf4b7d506a153202c411a91fa57778901d1ce5ec1ce10ee7fe1e8d1f0`  
		Last Modified: Tue, 14 Jan 2025 23:45:00 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3417a1709badaeb53ecd647dcd537f0afcb3e8c33e24d4fe508b1413a2b8e7c`  
		Last Modified: Tue, 14 Jan 2025 23:45:00 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3723505b9c91d8260cdd509e429243a831cc31c3276cc83262fe711340d4c8`  
		Last Modified: Tue, 14 Jan 2025 23:45:00 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881d31b5e828a961221df8527cc8fc5782978df421c98e4b7f019864ce532d47`  
		Last Modified: Tue, 14 Jan 2025 23:45:12 GMT  
		Size: 208.8 MB (208806782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18930c450c2c65ad2a894a777b6d4dea342e032e098029dfd9e39543ebbfe58f`  
		Last Modified: Tue, 14 Jan 2025 23:45:00 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
