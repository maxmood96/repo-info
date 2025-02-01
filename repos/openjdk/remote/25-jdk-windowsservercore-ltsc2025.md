## `openjdk:25-jdk-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:33f044666d68ea8b6a0cf1c02f32bd50408f40fdd5c1cd8ed6ed46a1775cb0ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `openjdk:25-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull openjdk@sha256:e87db0ac62015739354288728d009b0542574e53f037431bad9b122edf18bbe1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2708935320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1a7ec8d15e6a2addf248573e5ad58d3a1f71b2c9f8effdce74ebe16a7e698b1`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Fri, 31 Jan 2025 22:29:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Jan 2025 22:29:17 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 31 Jan 2025 22:29:17 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 31 Jan 2025 22:29:22 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 31 Jan 2025 22:29:23 GMT
ENV JAVA_VERSION=25-ea+8
# Fri, 31 Jan 2025 22:29:23 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/8/GPL/openjdk-25-ea+8_windows-x64_bin.zip
# Fri, 31 Jan 2025 22:29:24 GMT
ENV JAVA_SHA256=3ea9473d90c2a51f51d40081e60eb97a8fd26b8f787d9b44a51f102714942cf6
# Fri, 31 Jan 2025 22:29:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 31 Jan 2025 22:29:42 GMT
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
	-	`sha256:789e240b6ca4edd94eea73033ddd6cb81efdbfdbae912cc81c0f2ae8ec56aca1`  
		Last Modified: Fri, 31 Jan 2025 22:29:45 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b043d0d44a4013839901be345a9d6a2d55ffe90e1ea55a4c4176aaba1a21c9`  
		Last Modified: Fri, 31 Jan 2025 22:29:45 GMT  
		Size: 393.7 KB (393675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c8730d8e619a13b07df385ef40a92ab645cce8da882d24892add7f16f3bee0`  
		Last Modified: Fri, 31 Jan 2025 22:29:45 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8539e717fe13546ef9445e7add6a35dd448f93134bc0874c639d648b6e8f44c`  
		Last Modified: Fri, 31 Jan 2025 22:29:45 GMT  
		Size: 368.1 KB (368114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23c169841c8cc6b79796217126bcd4ac55c6aacd68aba4a10055e0fc07c4307e`  
		Last Modified: Fri, 31 Jan 2025 22:29:44 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992a9337b2a91091e54b93c62ccd1c38e707c927a24880aa9d865f2cda537935`  
		Last Modified: Fri, 31 Jan 2025 22:29:44 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df25961ef7a8e26f93b3d8cc656e314925c42aa41e3ebbf2417f250c75c1a6af`  
		Last Modified: Fri, 31 Jan 2025 22:29:44 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd0a33e292e7a3d4ec393b35f91288306deec07b4c092bd20d32d81bd00c9873`  
		Last Modified: Fri, 31 Jan 2025 22:29:57 GMT  
		Size: 207.9 MB (207888192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a145308567f61aacb54508d6f9fe3e10a2cfd07d2f6a0fec7db4df1295f92efb`  
		Last Modified: Fri, 31 Jan 2025 22:29:44 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
