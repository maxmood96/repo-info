## `eclipse-temurin:8-jdk-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:e96f2e17ef186a89a31c12415cbc0d71df64948e9651940ead93804f2bfac9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `eclipse-temurin:8-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull eclipse-temurin@sha256:89b828fc4b682e064ea243e16012062dd6cb1d661af24db72dd28eae249e444b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2454092834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c3bba0b036939e8f73f2573f21528ded27143fa860a01a5b22e40ac7bac8a3e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Fri, 31 Jan 2025 01:29:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Jan 2025 01:29:29 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Fri, 31 Jan 2025 01:31:07 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_windows_hotspot_8u442b06.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_windows_hotspot_8u442b06.msi ;     Write-Host ('Verifying sha256 (fac13d03d3d193509d82ef964060c21f2b20bc0ca3419ecc5cb3ef71283f2f94) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'fac13d03d3d193509d82ef964060c21f2b20bc0ca3419ecc5cb3ef71283f2f94') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 31 Jan 2025 01:31:15 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9877880b4b706baf69da2f27306d926c59da2e90f862853c68d43b815a6465dd`  
		Last Modified: Fri, 31 Jan 2025 01:31:19 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15aae7fb37d29751d88118a635a2a75b76220e5049668c28ab76f133cd77ccd3`  
		Last Modified: Fri, 31 Jan 2025 01:31:19 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace0285e8d6429e4b1d4e095752c050b72e1374fa43c4dae5df981912d615517`  
		Last Modified: Fri, 31 Jan 2025 01:31:27 GMT  
		Size: 191.4 MB (191377235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cdaf3bc8474c356c7e1e7b16dbd43a59ffcd94d315eaafc4467c93f24a2957d`  
		Last Modified: Fri, 31 Jan 2025 01:31:19 GMT  
		Size: 327.7 KB (327694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
