## `openjdk:24-ea-34-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:ad8deef6bf675d99200e9b4180189cc61e17ba24c6611e2e7eb4fea028657869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `openjdk:24-ea-34-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull openjdk@sha256:949d6fcaf07b8b558d7bae163d2b21cbaa6ac3f84ccac083e232e64c9d25ac92
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2331788536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e06f86c0eb243b22cb57dfd035748ca7768aaf1f34d047bd78e21941c208d519`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Fri, 31 Jan 2025 22:25:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Jan 2025 22:26:39 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 31 Jan 2025 22:26:40 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 31 Jan 2025 22:26:48 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 31 Jan 2025 22:26:49 GMT
ENV JAVA_VERSION=24-ea+34
# Fri, 31 Jan 2025 22:26:49 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/34/GPL/openjdk-24-ea+34_windows-x64_bin.zip
# Fri, 31 Jan 2025 22:26:50 GMT
ENV JAVA_SHA256=190d1d3c9dc679675ebbe68fc9936e9f17471cd4c161f9f7a3fefc1750bd74d7
# Fri, 31 Jan 2025 22:27:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 31 Jan 2025 22:27:21 GMT
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
	-	`sha256:3fc7c733b89b7e736b0b5a266c1f99c8a7798d2d6edd325be22d8037144d5d64`  
		Last Modified: Fri, 31 Jan 2025 22:27:29 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6784abec728903a90226592058d6e3a953b7b04f5dddc4550f8c51000e1ac28f`  
		Last Modified: Fri, 31 Jan 2025 22:27:28 GMT  
		Size: 341.2 KB (341218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cbd6d16f0f895da13abd95db98cda229b101ce041bf5d6084f486584bc5be6c`  
		Last Modified: Fri, 31 Jan 2025 22:27:28 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:498a3c7f8d58e7db125fe24adb1de59c43aee6039a482b6157c50e1b87bba24b`  
		Last Modified: Fri, 31 Jan 2025 22:27:28 GMT  
		Size: 331.9 KB (331923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc50fbd4c6344c112c5e713ae4b06eabb0fc429893d84620392fe76a23f28021`  
		Last Modified: Fri, 31 Jan 2025 22:27:26 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40c64a82ccf0be890a984428f35deb743569e457266c1bdb1913a8ca9fc21327`  
		Last Modified: Fri, 31 Jan 2025 22:27:26 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d45e0af3e3f3b01f3bee821334928d7abaabc7072020cb4e745c1fbeee5759d`  
		Last Modified: Fri, 31 Jan 2025 22:27:26 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b62cade77897a0b07171c69803ec21bacc3c13a948cc0165c49c23b39dc725`  
		Last Modified: Fri, 31 Jan 2025 22:27:37 GMT  
		Size: 208.9 MB (208895437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95669b3f8c264b5f8fdeb40bff2167058a420ac5f9c45e4c652b0c8d5eb224fd`  
		Last Modified: Fri, 31 Jan 2025 22:27:26 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
