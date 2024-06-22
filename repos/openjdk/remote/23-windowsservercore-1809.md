## `openjdk:23-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:978caf4867b9f3d6705657c43be5b42d933755dee51b52d933ef09ee4972ea3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `openjdk:23-windowsservercore-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull openjdk@sha256:5ecbfbaf82056d975cb6d10c8746f8142adee56d19766c973c3af3db5f1a4e2d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2427986080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f26fdab5344dd26941b93c5492f3cab1f05c6458cfcfde8347f5358300c5ddbc`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Sat, 22 Jun 2024 01:10:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Jun 2024 01:12:08 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 22 Jun 2024 01:12:09 GMT
ENV JAVA_HOME=C:\openjdk-23
# Sat, 22 Jun 2024 01:12:29 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 22 Jun 2024 01:12:30 GMT
ENV JAVA_VERSION=23-ea+28
# Sat, 22 Jun 2024 01:12:31 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/28/GPL/openjdk-23-ea+28_windows-x64_bin.zip
# Sat, 22 Jun 2024 01:12:32 GMT
ENV JAVA_SHA256=704ac9f8ab6e8ce660c18ab24a7b5cb2f0c8f7f9a51a2962efd7cadcf0d68bda
# Sat, 22 Jun 2024 01:13:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 22 Jun 2024 01:13:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7752da1668f307c54f50c29469fd1e18974e3d14d0c0b00f30c642cf63f3fd8c`  
		Last Modified: Sat, 22 Jun 2024 01:13:15 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff9bf45831e9ba75ffa71459e3b729c8fc725fba907f8a5326320864b083cbf`  
		Last Modified: Sat, 22 Jun 2024 01:13:15 GMT  
		Size: 506.5 KB (506518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03974dabd4e770cb1e032783acc4f417416db09c4043946592515fb10c3f5a73`  
		Last Modified: Sat, 22 Jun 2024 01:13:15 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d59fd7eca73eee41d4658e7753118e37f199d4fdf9df0c518e3f18b33b39c3b3`  
		Last Modified: Sat, 22 Jun 2024 01:13:15 GMT  
		Size: 354.1 KB (354079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5454114cf8b5e73ddbdcf4568737aab36e5da4d30641060cc4a90d55b82c58b4`  
		Last Modified: Sat, 22 Jun 2024 01:13:14 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ab1ab9dc684b6ccc98bce6bd4785f7af3a079b717d2a33c62e0c00073b0697`  
		Last Modified: Sat, 22 Jun 2024 01:13:14 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f805f7c4af313ea751ba03fb2100fbd92c18a7e97b3a216ebc3c30f7a8eb203`  
		Last Modified: Sat, 22 Jun 2024 01:13:14 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e45cf89b773b510db54049d5ee7f8a72ac2cfb5ea4a58cf3beb1be8f7065580`  
		Last Modified: Sat, 22 Jun 2024 01:13:25 GMT  
		Size: 206.4 MB (206436472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408900f1fa3d549abe3ad07ec50cfc53de901d7c7153601c087542195039f241`  
		Last Modified: Sat, 22 Jun 2024 01:13:14 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
