## `eclipse-temurin:21-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:e99465f30ccb2a7d97dd5beecd9e0422a614119affedda1456dec004a9257af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2529; amd64

### `eclipse-temurin:21-windowsservercore-ltsc2022` - windows version 10.0.20348.2529; amd64

```console
$ docker pull eclipse-temurin@sha256:b946bb25b6dc7c90bfa054ebe4b3c8f9b72c83c18b7416bbd620b262c824a45a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2498934507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84730f47206f049be6df64a8828fcdfb61e1cea12087ebdfb382e188914b7030`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 19 Jun 2024 19:58:05 GMT
RUN Install update 10.0.20348.2529
# Sat, 22 Jun 2024 00:33:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Jun 2024 00:43:37 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Sat, 22 Jun 2024 00:44:42 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_x64_windows_hotspot_21.0.3_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_x64_windows_hotspot_21.0.3_9.msi ;     Write-Host ('Verifying sha256 (264db89e74213f3ea2d7b7379d1c2ac346797d03b4d88cbf4ce72c3ff96477a1) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '264db89e74213f3ea2d7b7379d1c2ac346797d03b4d88cbf4ce72c3ff96477a1') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Sat, 22 Jun 2024 00:45:09 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Sat, 22 Jun 2024 00:45:10 GMT
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
	-	`sha256:8b4326efd24d64d6a2efa78c581696b3d528dfcf784a3d6605e621e343b62e16`  
		Last Modified: Sat, 22 Jun 2024 00:59:51 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2789df543302a6ab2c7c38b2605ae77577dfe09c69ea045c10ed0f990f72547`  
		Last Modified: Sat, 22 Jun 2024 01:04:21 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc6d41fb5b7ea4c9b4c9a73a43e362e84a3cf4c66292b3cfecbb7f95d546acb1`  
		Last Modified: Sat, 22 Jun 2024 01:04:48 GMT  
		Size: 380.5 MB (380462971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a66472824f7da1bf433a30428250fb8077d96304e22bf0b3fba34ee79109d7`  
		Last Modified: Sat, 22 Jun 2024 01:04:21 GMT  
		Size: 277.0 KB (276983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:287810d7e17169fa0f33585bf4fb025fe4c9c74bf9ba66d1a1f1ffa9b3313cfd`  
		Last Modified: Sat, 22 Jun 2024 01:04:21 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
