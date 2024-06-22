## `openjdk:23-ea-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:ca8b3e6622a713f20be3d6d79bd605fdae46f8355f2a3dca2ee9f4d9ba66335c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2529; amd64

### `openjdk:23-ea-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.2529; amd64

```console
$ docker pull openjdk@sha256:16dba13ccc00d5cfb8b7dbeac2120972eecca171c9331883c345a5e58f51f95b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2325288275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78d50ab2529565bb55e87e9296593b8ed796f7ee73c0cc45fdedaf920e6728e5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 19 Jun 2024 19:58:05 GMT
RUN Install update 10.0.20348.2529
# Sat, 22 Jun 2024 01:03:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Jun 2024 01:03:24 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 22 Jun 2024 01:03:24 GMT
ENV JAVA_HOME=C:\openjdk-23
# Sat, 22 Jun 2024 01:03:32 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 22 Jun 2024 01:03:33 GMT
ENV JAVA_VERSION=23-ea+28
# Sat, 22 Jun 2024 01:03:34 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/28/GPL/openjdk-23-ea+28_windows-x64_bin.zip
# Sat, 22 Jun 2024 01:03:35 GMT
ENV JAVA_SHA256=704ac9f8ab6e8ce660c18ab24a7b5cb2f0c8f7f9a51a2962efd7cadcf0d68bda
# Sat, 22 Jun 2024 01:03:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 22 Jun 2024 01:03:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb373ec9afdfc5f09b9380d981e0c61f9c7b48537b887135c7c66810086e705e`  
		Last Modified: Fri, 21 Jun 2024 00:27:54 GMT  
		Size: 729.6 MB (729591500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983a98cf25427013920fc3e36c3dbb9c38966e4a2e2e88c3d9bf6b89ae6721b6`  
		Last Modified: Sat, 22 Jun 2024 01:04:04 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe14bf4a33db5d49f0eae2b4ab658eef7fa69ff29dc2249f6cac4dca04ef500b`  
		Last Modified: Sat, 22 Jun 2024 01:04:04 GMT  
		Size: 349.0 KB (349042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa25722288e929dead99d0af28fedd68db29a83a15a6fc82c01c1f63f41088e`  
		Last Modified: Sat, 22 Jun 2024 01:04:04 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456957229669ea75bfa1b1bd22c6a025757bbd15ec641a09c333e54f6f97ac57`  
		Last Modified: Sat, 22 Jun 2024 01:04:03 GMT  
		Size: 334.9 KB (334949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16066bf038d34ce1a96e3702f0a20c1baf516c6ef48ab848da4d72090a0de1cf`  
		Last Modified: Sat, 22 Jun 2024 01:04:02 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb711763b50e56853b2c9aced18fb656181e74d2daedc5cf82b89a89db0d3f8`  
		Last Modified: Sat, 22 Jun 2024 01:04:02 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b6ed9c13011e15c96f0a13cdcb6844ea7b090e91387071ba4d1ffc61ab0ee0b`  
		Last Modified: Sat, 22 Jun 2024 01:04:02 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de7d89433b7d9903a1a4e6e3bf224f09d21ac2d509c1813855a2834e28d7276`  
		Last Modified: Sat, 22 Jun 2024 01:04:13 GMT  
		Size: 206.4 MB (206406088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfc61e90b4725ea812e1af2369b9db47373772cd30aa554e698b3da6e6adf8a5`  
		Last Modified: Sat, 22 Jun 2024 01:04:02 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
