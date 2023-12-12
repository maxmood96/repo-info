## `openjdk:23-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:3a8eb5357c2a807910400c39b16e489b45ade46e9d9ea97f676c63a3434060c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2113; amd64

### `openjdk:23-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.2113; amd64

```console
$ docker pull openjdk@sha256:c00bf0a36bff6b08ec8730d349dcab30a493b6388af56f01e8c5099e0df115c4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2085221270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70ed0bf4034d404da2a6c1ad57e40350f6936edbdccd85e8cf34def5bf29e7c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 09 Nov 2023 06:47:20 GMT
RUN Install update 10.0.20348.2113
# Thu, 16 Nov 2023 01:36:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Nov 2023 05:18:36 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 12 Dec 2023 20:14:59 GMT
ENV JAVA_HOME=C:\openjdk-23
# Tue, 12 Dec 2023 20:15:25 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 12 Dec 2023 20:15:26 GMT
ENV JAVA_VERSION=23-ea+1
# Tue, 12 Dec 2023 20:15:27 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/1/GPL/openjdk-23-ea+1_windows-x64_bin.zip
# Tue, 12 Dec 2023 20:15:28 GMT
ENV JAVA_SHA256=b60d20ad423ec31c88a18679854a31bdef66003224227d86dcbd10781fe14db1
# Tue, 12 Dec 2023 20:16:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 12 Dec 2023 20:16:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7989ef2c4cfb06d845746a3c3660481ea84d3f5c8216041855ce528f0ac4015c`  
		Last Modified: Tue, 14 Nov 2023 20:43:13 GMT  
		Size: 498.2 MB (498182566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbeb193d02c2ca7f9a9ea438fbf1bcdb6ea4a6fea626713330fd1ebb514424f`  
		Last Modified: Thu, 16 Nov 2023 02:25:14 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c484d21f80984bc956d2a7ca187c7250676fd3af73a362efb91125bb6255aa10`  
		Last Modified: Thu, 16 Nov 2023 05:26:11 GMT  
		Size: 453.2 KB (453223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a02f84b7204ed0cac02a5fa90f2d2f2ac67657e8b579aa9e1ba7e04ad05f7a4`  
		Last Modified: Tue, 12 Dec 2023 20:21:48 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e79a392d9faeee19306f49ea010c9ed47d0992bc82c841346d28babc2a14016b`  
		Last Modified: Tue, 12 Dec 2023 20:21:48 GMT  
		Size: 279.3 KB (279315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f08d5eaeeac437d7edc41dcdf37f597f6a9f86140ed8c6f549caa4c4e1a6f9e`  
		Last Modified: Tue, 12 Dec 2023 20:21:45 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd14f20c1c23b95d44dea037043c274fc4a3dae1fbf0da07b45c61f4f727041`  
		Last Modified: Tue, 12 Dec 2023 20:21:46 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ac8cb6d954d888cae48b34cc1ee422686986f5e1d9e6a5688783445479bbcd2`  
		Last Modified: Tue, 12 Dec 2023 20:21:46 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610badfeac664e0f54350c8d35e4307dfe3940255213607884fcbbe68bd25008`  
		Last Modified: Tue, 12 Dec 2023 20:22:03 GMT  
		Size: 197.7 MB (197698963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3f9191c324ab3825f45c09ca4781a637511b0cc607b5c47761850f55f48420`  
		Last Modified: Tue, 12 Dec 2023 20:21:46 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
