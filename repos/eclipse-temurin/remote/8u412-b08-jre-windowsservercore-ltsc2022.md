## `eclipse-temurin:8u412-b08-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:9640ab2896bf04811940d891a39e5ae73cf43321140569bb9ec4350c976361ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `eclipse-temurin:8u412-b08-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull eclipse-temurin@sha256:a7936abfd26886e8848a97d3a4555c2d8242cd04169b71c0043ef68b2f867467
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2185297161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e79f1cccadf04c14f79587ab92fc4ed1d0e32f27e8a50eee6cba961b53fa0c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 15 May 2024 19:36:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 19:36:44 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Wed, 15 May 2024 19:43:28 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_x64_windows_hotspot_8u412b08.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_x64_windows_hotspot_8u412b08.msi ;     Write-Host ('Verifying sha256 (d6ab48ee1a4f4fa7f2d64e2ecffd2548b7116f7857f1d6352520ed1bb5fbc8f7) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'd6ab48ee1a4f4fa7f2d64e2ecffd2548b7116f7857f1d6352520ed1bb5fbc8f7') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 15 May 2024 19:43:53 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241bde7d4f3acae2008c131651582fc2bb7b130e1f5b90583702d17cad8acd2f`  
		Last Modified: Wed, 15 May 2024 20:42:14 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0561045a1574c8c86de9bcf12d5c76710dbe3045deec80fd994ae6ddbd23de4a`  
		Last Modified: Wed, 15 May 2024 20:42:14 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a739922cb700b0d3385174590f3c22dce25511c97749ddca358d7c6d1e9abb`  
		Last Modified: Wed, 15 May 2024 20:46:37 GMT  
		Size: 72.3 MB (72335925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3056d9f307b5cf793513b097a7b94fd3780245c4aa6b021d6090109afe3fc1a9`  
		Last Modified: Wed, 15 May 2024 20:46:29 GMT  
		Size: 287.0 KB (287035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
