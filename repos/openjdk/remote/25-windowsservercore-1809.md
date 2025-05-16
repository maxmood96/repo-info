## `openjdk:25-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:918a81766a4048f109a5d3024eaea0f3db04053d7d30d7b603311ba6286dc8b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `openjdk:25-windowsservercore-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull openjdk@sha256:3a151d1910883934005c77c2a25ac085a53340792e666475fb70b663a28cb89b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2393745743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3391de461880779aceee2c7dc465c4c4237ff6c9c72ea8b5b3a3ffe2a9460f69`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Fri, 16 May 2025 21:02:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 16 May 2025 21:02:55 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 16 May 2025 21:02:56 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 16 May 2025 21:03:03 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 16 May 2025 21:03:03 GMT
ENV JAVA_VERSION=25-ea+23
# Fri, 16 May 2025 21:03:04 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/23/GPL/openjdk-25-ea+23_windows-x64_bin.zip
# Fri, 16 May 2025 21:03:05 GMT
ENV JAVA_SHA256=903e77b6d79a2c808e32a4111a54802e149b11e39d15629d7a04ccfb97e4c79b
# Fri, 16 May 2025 21:03:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 16 May 2025 21:03:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95a939635fd6bec8c1562dcdbdde2fdb64095d1be9873313939c878db6f7279`  
		Last Modified: Thu, 15 May 2025 19:24:26 GMT  
		Size: 463.4 MB (463449115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c94e107aaec5a76637bb9d0822c9cf6b2ba8a57634d1749688bd1dc825789b`  
		Last Modified: Fri, 16 May 2025 21:04:33 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ddd89a16a6372003ab30aba8de26edb75a9a24be6a9cf27943d0b396c5e121a`  
		Last Modified: Fri, 16 May 2025 21:04:33 GMT  
		Size: 365.9 KB (365877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e337606391fa081a0fb2d5933133352f37d773af4352f25ed94d74955b4c3a5`  
		Last Modified: Fri, 16 May 2025 21:04:33 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe4a761f944bd3a3d72fb28014db2c4303e811c7d5b19a8e25ed3bb8be879d7`  
		Last Modified: Fri, 16 May 2025 21:04:34 GMT  
		Size: 342.7 KB (342711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ccefbb2ed9e2cffe4fbeadaac0fd112efebb0ac08ea36f73d84c467a501572`  
		Last Modified: Fri, 16 May 2025 21:04:34 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38c5cb9e3ef8d3bdc6eec3a5a43861d989bed9bcf867527dcd1492f94d50c37b`  
		Last Modified: Fri, 16 May 2025 21:04:34 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751e01f472e821f6a073a42f3e97d1f7a8a91475e364ce3240850c5228a792ca`  
		Last Modified: Fri, 16 May 2025 21:04:34 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c4a64c519aff730c877c854a072bff5a984a0cca1871a29da710ba81035fd31`  
		Last Modified: Fri, 16 May 2025 21:08:24 GMT  
		Size: 209.3 MB (209311769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b55eb9e18404d9ac9178ea4b2bf47a852d1a2cdad51d15bfa3d50215e28ca0`  
		Last Modified: Fri, 16 May 2025 21:04:34 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
