## `openjdk:24-jdk-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:9b09e4452c063c2589bf20bd5b90ab7b8cb8bf9f8e752a9dd37abdf850838393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `openjdk:24-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull openjdk@sha256:2af2b4d23bd8699ba40cafa900bbcd11415f14ad46cf5c2dd83480cb78eefca8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2709970676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46a9d8fd55b50baa1d61f3d6c490edb039f0bdf652e305734faa3524ab506167`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Thu, 23 Jan 2025 22:29:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 22:29:58 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 23 Jan 2025 22:29:59 GMT
ENV JAVA_HOME=C:\openjdk-24
# Thu, 23 Jan 2025 22:30:05 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Thu, 23 Jan 2025 22:30:06 GMT
ENV JAVA_VERSION=24-ea+32
# Thu, 23 Jan 2025 22:30:07 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/32/GPL/openjdk-24-ea+32_windows-x64_bin.zip
# Thu, 23 Jan 2025 22:30:07 GMT
ENV JAVA_SHA256=e5f13b2b408e1c98310b5fac3025ff52a576a8ca77ad40ec8a1e90d8d1ca3094
# Thu, 23 Jan 2025 22:30:25 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 23 Jan 2025 22:30:26 GMT
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
	-	`sha256:45d31051af3441fff8ceffe0d7d229bf6e16c93fe8249510aa7f14ab1c3da146`  
		Last Modified: Thu, 23 Jan 2025 22:30:32 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ace684bc0a5a15ffdea29c2135185762630057b05c52fcbec37a2503ae02862`  
		Last Modified: Thu, 23 Jan 2025 22:30:33 GMT  
		Size: 395.3 KB (395330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec84ca491f6f2aeef424ec1a638fa1ecec9b9a906132c6c5e88e446b5463446`  
		Last Modified: Thu, 23 Jan 2025 22:30:32 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ffb09f553c2927b00078f8719ae798bab69a8461167ee360659363de6b85ae8`  
		Last Modified: Thu, 23 Jan 2025 22:30:32 GMT  
		Size: 383.0 KB (383045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d8d3ed832ef393390b14922c9f1c04dcedfc46ae34c717423f431964922ddb`  
		Last Modified: Thu, 23 Jan 2025 22:30:30 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b939e082500da86767bf0932f010d338880b23e9484103ff4e7c05a24f1e1e8d`  
		Last Modified: Thu, 23 Jan 2025 22:30:30 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bca0d37e61c9e1fcd62870bc1ffb1f1cb4692474d3c9d10724b734f405d3a31`  
		Last Modified: Thu, 23 Jan 2025 22:30:30 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6796d6f4ffb8f1caa42b408e494a5c5170d39b07d89b3a7bdde41f6738510674`  
		Last Modified: Thu, 23 Jan 2025 22:30:42 GMT  
		Size: 208.9 MB (208906925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef12dae2f1420cf78617dac6f90a0807b31399ff416986c33a46c6f2627f55f`  
		Last Modified: Thu, 23 Jan 2025 22:30:30 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
