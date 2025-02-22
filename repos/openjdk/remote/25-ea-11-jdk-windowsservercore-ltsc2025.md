## `openjdk:25-ea-11-jdk-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:e12deddb64b2023a330b80a3f9252d4ae238b054af655e9e9f2ca6e28cf35b0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `openjdk:25-ea-11-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull openjdk@sha256:29148395fcc22e96558eb5b2b34815728e6fade263d8a544b5b8c1a83e900ea5
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2709052943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c8de973d5de62ddc042b2050f71f748c168d25992bf47f06eb62c4c2e29afd9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Sat, 22 Feb 2025 00:31:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Feb 2025 00:31:32 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 22 Feb 2025 00:31:32 GMT
ENV JAVA_HOME=C:\openjdk-25
# Sat, 22 Feb 2025 00:31:39 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 22 Feb 2025 00:31:39 GMT
ENV JAVA_VERSION=25-ea+11
# Sat, 22 Feb 2025 00:31:40 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/11/GPL/openjdk-25-ea+11_windows-x64_bin.zip
# Sat, 22 Feb 2025 00:31:40 GMT
ENV JAVA_SHA256=7db003a6e122cc08ddd88b60142284f2461efe69b7007138277f55c2b4cf1d4a
# Sat, 22 Feb 2025 00:31:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 22 Feb 2025 00:31:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37ddd2d7a81fc53d954a9dd2d0c34b6dc11de32b78f776de50f9b8d3612777b`  
		Last Modified: Sat, 22 Feb 2025 00:32:03 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ccffd1373b539222b7f4bbfc6083f3e1847112d8175dd9bcf6d2f1d5e7e399`  
		Last Modified: Sat, 22 Feb 2025 00:32:04 GMT  
		Size: 401.1 KB (401147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab598190fdc93227bcd60de240df753030cb05380822e60fa0878c2acb361f70`  
		Last Modified: Sat, 22 Feb 2025 00:32:03 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb8cee35d5dc36789c3c29ff11a43d366bfdf5a263426f8d89ccc05ad7132c6b`  
		Last Modified: Sat, 22 Feb 2025 00:32:03 GMT  
		Size: 377.5 KB (377458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24c93e9bbcbcca94aba03552457f79655d9423967d17b5825b54bf288c5fcba`  
		Last Modified: Sat, 22 Feb 2025 00:32:02 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0edb3840e2336439da3190de915e1bf68a3719c90b08c86ef6a4ce8d79c32ebd`  
		Last Modified: Sat, 22 Feb 2025 00:32:02 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fef1732e979389c8693edc405d9d91bdf37cadcf8669c1543287c9493f124f23`  
		Last Modified: Sat, 22 Feb 2025 00:32:02 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68567142facd3ae450b9798fdacc53083f6e9e6cb4dcaceb9c778f0f61e716ef`  
		Last Modified: Sat, 22 Feb 2025 00:32:15 GMT  
		Size: 208.0 MB (207988864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caed0205b8d202632969b54b4f3d3c6e78043f5da7954ed95f2df333427f7661`  
		Last Modified: Sat, 22 Feb 2025 00:32:02 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
