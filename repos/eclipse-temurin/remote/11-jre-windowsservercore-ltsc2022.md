## `eclipse-temurin:11-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:786aebc769621ea19d10bc6bee4c87d8296a50afea65f78ad75aba69d9945988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3932; amd64

### `eclipse-temurin:11-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.3932; amd64

```console
$ docker pull eclipse-temurin@sha256:eb9a2434a64a41b4c431bee09ddd5e44ac411b43900b95c95652e19b634305f4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2355915304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f4e8f16f7647c9784858ae08e69002240788b846163ecad80113433c19d4317`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 05 Jul 2025 05:31:06 GMT
RUN Install update 10.0.20348.3932
# Wed, 09 Jul 2025 18:07:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jul 2025 18:07:09 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 09 Jul 2025 18:07:28 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_x64_windows_hotspot_11.0.27_6.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_x64_windows_hotspot_11.0.27_6.msi ;     Write-Host ('Verifying sha256 (08b8bcdf7f61f4276d90eccef6d70a4b73c25f0b4c2cdd2e6ddf15c24c087160) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '08b8bcdf7f61f4276d90eccef6d70a4b73c25f0b4c2cdd2e6ddf15c24c087160') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 09 Jul 2025 18:07:36 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b829944a73d1d8ad37eaa13c64bf9189b6895cc5b45b79bb3563fa325d94b6a7`  
		Last Modified: Wed, 09 Jul 2025 00:17:04 GMT  
		Size: 818.4 MB (818411069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba1c5998b6a72f54927430760c191e3eb70b7f2cc485fb313066dfdb059f6ce6`  
		Last Modified: Wed, 09 Jul 2025 19:08:13 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69277195d88e0c56ea717875d2171a8b944e38b861124c8afa2d7f7206543283`  
		Last Modified: Wed, 09 Jul 2025 19:08:13 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4556c9b96fa3c67bfaf6f3140ebcb928081cdb1e8d46c17508369fde81c673`  
		Last Modified: Wed, 09 Jul 2025 19:08:17 GMT  
		Size: 75.0 MB (74961325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2241f05b6c9a33e08c2633cceaad49c5e8b80418dc0051894dd10880946f6e56`  
		Last Modified: Wed, 09 Jul 2025 19:08:14 GMT  
		Size: 347.9 KB (347932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
