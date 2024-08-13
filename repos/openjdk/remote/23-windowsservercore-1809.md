## `openjdk:23-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:42734780552a43ef2a4f3b64d7d3f6ec54bc84a7b410c240c07e59b642c76f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `openjdk:23-windowsservercore-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull openjdk@sha256:88df5d409ff9a181a8cdaa4fe0762e0cbec0917afe9848277bf12b4fe9c24e07
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2452447898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb40c197d597dcbb7bdd23555f81eea2f0a4db5462e7e4fbff58b725ed8d838`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Tue, 13 Aug 2024 20:22:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Aug 2024 20:23:42 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 13 Aug 2024 20:23:43 GMT
ENV JAVA_HOME=C:\openjdk-23
# Tue, 13 Aug 2024 20:24:01 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 13 Aug 2024 20:24:01 GMT
ENV JAVA_VERSION=23
# Tue, 13 Aug 2024 20:24:01 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/36/GPL/openjdk-23_windows-x64_bin.zip
# Tue, 13 Aug 2024 20:24:02 GMT
ENV JAVA_SHA256=b18897bec6b1c6e0f639d95757eb0e3b0ec3d69720f6e4631874f2f9408075c5
# Tue, 13 Aug 2024 20:24:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 13 Aug 2024 20:24:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ea461e47505e6d80552039fa353c061374ee1e4a787b8fd39eae413b00d676`  
		Last Modified: Tue, 13 Aug 2024 20:24:43 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec235f678c457b9b63f4e3063293dd09753f918af8277fb45e18eb1e94f7d1d`  
		Last Modified: Tue, 13 Aug 2024 20:24:43 GMT  
		Size: 488.5 KB (488530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65a4db3505ecdfcd7fe910a9582573e43d4a9f2232b23f707133b0d4796e3fe`  
		Last Modified: Tue, 13 Aug 2024 20:24:42 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb0f8b9b20c346f4830189f12333c883cbc5c98fc3509db14da10ef2244010c2`  
		Last Modified: Tue, 13 Aug 2024 20:24:42 GMT  
		Size: 335.5 KB (335471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8a877757de33a773a410ec7974470fcf0b736b8931599faf05f54a8a30416f`  
		Last Modified: Tue, 13 Aug 2024 20:24:42 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af6053cb92cb5642dfba8066acc9c6710733a8b0f40b39f33cb7b08257fa178`  
		Last Modified: Tue, 13 Aug 2024 20:24:42 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78dbd5233bee791b33177018960430cd7a4f3d60fb4aa071f4aa91c2deeb4b62`  
		Last Modified: Tue, 13 Aug 2024 20:24:41 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fa829cd0ca01150e87729e82f589c595186ca7a8f636b467eecc2ff3bc9998f`  
		Last Modified: Tue, 13 Aug 2024 20:24:53 GMT  
		Size: 206.4 MB (206412834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1221680068eb05cf37ad39445aa0577e9e64fc3f723794cee69cff2062efdfa`  
		Last Modified: Tue, 13 Aug 2024 20:24:41 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
