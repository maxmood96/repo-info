## `openjdk:26-ea-27-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:c3ad885b7055a04f14b75b8c061a382498a2de57c233ab37054e890caaf0a04c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `openjdk:26-ea-27-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull openjdk@sha256:47bee49942bd227a9e99119c4fd1bbaf7b86d1ff667f2fb964dba7ccdb8c1f64
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1996398069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d153ec78e11124ef7400d45ce9722a37b4309d157997a19a07d6bd14dbf068`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Sat, 06 Dec 2025 00:35:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 06 Dec 2025 00:36:13 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 06 Dec 2025 00:36:14 GMT
ENV JAVA_HOME=C:\openjdk-26
# Sat, 06 Dec 2025 00:36:21 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 06 Dec 2025 00:36:22 GMT
ENV JAVA_VERSION=26-ea+27
# Sat, 06 Dec 2025 00:36:24 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/27/GPL/openjdk-26-ea+27_windows-x64_bin.zip
# Sat, 06 Dec 2025 00:36:24 GMT
ENV JAVA_SHA256=5fc8523fafe0bbe81e010d1bd57b12836c42cdd1f017e4492f67d56bde06f86a
# Sat, 06 Dec 2025 00:37:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 06 Dec 2025 00:38:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8462076761531ece541cabbff8aa81904d45ff8a160c631ad6c756c28992e1c1`  
		Last Modified: Sat, 06 Dec 2025 00:45:14 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed8504190794f5132138626e0d39aa6ce0ab2f2ea2b6097c6a0f0a9a46bd9fa5`  
		Last Modified: Sat, 06 Dec 2025 00:45:14 GMT  
		Size: 503.4 KB (503450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6b5f8d98f40b65f69ab8cab35c598883e94cac6ff276fb4f3ca26d843e41ea`  
		Last Modified: Sat, 06 Dec 2025 00:45:15 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b34eb090ef28780069b786a3fc78acd5351a4ed41b59355d32ebf2bab9a16a`  
		Last Modified: Sat, 06 Dec 2025 00:45:14 GMT  
		Size: 350.4 KB (350408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ce898cb9986365a8bd5cf55ce6fbc64841de2ad892b399ec872b0423f0d822`  
		Last Modified: Sat, 06 Dec 2025 00:45:14 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a688f845b597995cc8fbdeb016b93a4e6e2b703701455024f7d16c64fe40cbbf`  
		Last Modified: Sat, 06 Dec 2025 00:45:14 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2bbed5d893c469cfd0a51ca4278e1214afc683aaf76b1744190f29aa2ced43d`  
		Last Modified: Sat, 06 Dec 2025 00:45:14 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0195d684db06b7aff47c6bdcb2dacef9d691dccaaa757924d10d31a9e6a91c42`  
		Last Modified: Sat, 06 Dec 2025 00:45:32 GMT  
		Size: 225.6 MB (225574825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a8d5b08796e1e5944fcedfe5d0dd6c786d2281633635a7f39509ff33e481253`  
		Last Modified: Sat, 06 Dec 2025 00:45:14 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
