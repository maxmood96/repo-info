## `openjdk:26-ea-21-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:f6e0f83fdf235835ea9714a93e7fe7b90c6d4d7115658e86bb97eddb57cbd0bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `openjdk:26-ea-21-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull openjdk@sha256:1bbf04e4e5a771895498db9fcf41b59e7748af6b45b5c69912c234ebf8c653c3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1799619313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92df6ec0ec5fa005395b6f75d9f1bd83627e58c4eb09af7c1b72d5f2db3846bc`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 23:39:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 23:39:23 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 24 Oct 2025 23:39:24 GMT
ENV JAVA_HOME=C:\openjdk-26
# Fri, 24 Oct 2025 23:39:30 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 24 Oct 2025 23:39:31 GMT
ENV JAVA_VERSION=26-ea+21
# Fri, 24 Oct 2025 23:39:32 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/21/GPL/openjdk-26-ea+21_windows-x64_bin.zip
# Fri, 24 Oct 2025 23:39:32 GMT
ENV JAVA_SHA256=25b332cae815558e365575910625e421a10ecbf655f0ed2d480d42f3224e9b93
# Fri, 24 Oct 2025 23:40:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 23:40:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e49ff08bad79abee2117ad31238f872fddee88f6fdb356a9bf85922ae18b21a`  
		Last Modified: Fri, 24 Oct 2025 23:45:26 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d00f1ffb286b93ed8fb3abda82d1bba997eea7bdad3f84da36153530be93af`  
		Last Modified: Fri, 24 Oct 2025 23:45:26 GMT  
		Size: 498.5 KB (498509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4d5a38902f5ad04ef42c5b6206d70c1c23fead687c17ec1cb2de78f388ab200`  
		Last Modified: Fri, 24 Oct 2025 23:45:26 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb8940908bf17621a804ede266539b32be0328fa10a9743777a5911ee909e8a`  
		Last Modified: Fri, 24 Oct 2025 23:45:26 GMT  
		Size: 337.2 KB (337248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506982969c9c4d44c21507b061fd1fb11c66157243c1bcff1c428ac027f91338`  
		Last Modified: Fri, 24 Oct 2025 23:45:26 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af15034e30f9b4118d54fcffb09437a11e44b3dd837db12762ffb9e64d06f489`  
		Last Modified: Fri, 24 Oct 2025 23:45:26 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f64b4f68ac66f9a0c0773af8baa830294d0652d7b80701db4e11cd8378df8a`  
		Last Modified: Fri, 24 Oct 2025 23:45:27 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276e593b506bb559cfd6dc44aa84bd56ad04d44afe6d48be1db1abd87e95c3f8`  
		Last Modified: Sat, 25 Oct 2025 00:12:45 GMT  
		Size: 221.6 MB (221582749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d3c22566ecfd63fb6c5966e78a655487774f547f0ff64b517b38ca1ce041ac2`  
		Last Modified: Fri, 24 Oct 2025 23:45:26 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
