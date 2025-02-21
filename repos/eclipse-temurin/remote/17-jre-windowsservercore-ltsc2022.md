## `eclipse-temurin:17-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:e1cdf72f322ba85c49f3ddbb5fd605bf093f4232c08af3cb4c0b890c781a6f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `eclipse-temurin:17-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull eclipse-temurin@sha256:03e22172a3edc8c49d102b7710512eabf3eca19f318fdde0da5f04a273a1aabe
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2339285841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5214926f974ef581784b8a51f34ec9c4f41f5df7e7f96072af2e5207a7cad901`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:35:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:35:23 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 13 Feb 2025 00:35:41 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_windows_hotspot_17.0.14_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_windows_hotspot_17.0.14_7.msi ;     Write-Host ('Verifying sha256 (6a81df58247baeec4153e746b68af5b8618e50ed51a59b4c9e0c1b025edd4ad8) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '6a81df58247baeec4153e746b68af5b8618e50ed51a59b4c9e0c1b025edd4ad8') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 13 Feb 2025 00:35:47 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0980bb5edfc6d75dc6674691818d95bfcdd1abce7ee4430dcfa7e732e7c77619`  
		Last Modified: Thu, 13 Feb 2025 00:35:51 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2210c40f2d4af1c37d0ec52de440cf9520ee5b53053ed0096d9ecdd75c34e358`  
		Last Modified: Thu, 13 Feb 2025 00:35:51 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408906c585205ed04172eb0be24f481ad5f55508be64f3c886ef8d2ad60d5824`  
		Last Modified: Thu, 13 Feb 2025 00:35:57 GMT  
		Size: 75.1 MB (75077844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c8868e876a6b3c1ce12b4a87dbca983fa4ab1acae9390a028b5b96d2fec326f`  
		Last Modified: Thu, 13 Feb 2025 00:35:51 GMT  
		Size: 347.4 KB (347420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
