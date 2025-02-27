## `eclipse-temurin:17-jdk-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:6f3b6a488c2470eb3d1cc85669eeaffe2905293027f1050cbf61a3c743fa617f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `eclipse-temurin:17-jdk-windowsservercore` - windows version 10.0.20348.3207; amd64

```console
$ docker pull eclipse-temurin@sha256:1e6f81dbb5da783cede921d674153420bd44af056b6461c2bb95d4101d2f5954
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2619359265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ea3c8d2408c2a0bf222ef208bb8319c60931cce38c149b62f394dd1575844a9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:37:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:37:04 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 13 Feb 2025 00:37:31 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_windows_hotspot_17.0.14_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_windows_hotspot_17.0.14_7.msi ;     Write-Host ('Verifying sha256 (021589cc7d85392b24c3992331d84b25f0b1c1e6603dae07594abb97105fa67f) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '021589cc7d85392b24c3992331d84b25f0b1c1e6603dae07594abb97105fa67f') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 13 Feb 2025 00:37:39 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:37:39 GMT
CMD ["jshell"]
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
	-	`sha256:fbb3622a83714955a687cb7ec226e3ab992e603ea79b8fcd0d6fd6992d691c29`  
		Last Modified: Thu, 13 Feb 2025 00:37:42 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:252081758b4a066502ced6e5b45f1d74318511d68710fe1b13c73ba98379f61f`  
		Last Modified: Thu, 13 Feb 2025 00:37:42 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf81f481771c62f669878a9b69f65d4c3516c84176e7406ee4c20573907a7f5a`  
		Last Modified: Thu, 13 Feb 2025 00:37:56 GMT  
		Size: 355.1 MB (355118792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8238e86d2d6528e8c1f8e2632c58f2fc08ec8e59ee77ab88a0de5fdb6cd1534`  
		Last Modified: Thu, 13 Feb 2025 00:37:42 GMT  
		Size: 378.6 KB (378617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ec27aad878b8110708bec6a9d9795acac9fb051bd322451917b3b52d861faaa`  
		Last Modified: Thu, 13 Feb 2025 00:37:42 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jdk-windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull eclipse-temurin@sha256:3db2cf6ea04bdd2c59fce3bed8ce54353e3b9c8e287daf5e876765235463ef4a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2495893858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6c1ef2e48769f35ca6501a10f6ce4f2510da4dd82786f63a598fd19437093b6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:31:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:31:02 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 13 Feb 2025 00:31:42 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_windows_hotspot_17.0.14_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_windows_hotspot_17.0.14_7.msi ;     Write-Host ('Verifying sha256 (021589cc7d85392b24c3992331d84b25f0b1c1e6603dae07594abb97105fa67f) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '021589cc7d85392b24c3992331d84b25f0b1c1e6603dae07594abb97105fa67f') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 13 Feb 2025 00:31:51 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:31:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaf6d6b858d1221f5f91ab4bb9745fd6125db2b214d215cfea7dd82326c48b4`  
		Last Modified: Thu, 13 Feb 2025 00:31:56 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e153ad8f0bf2b7052cfa1c1ea4dbf7a7abade6561ceb81c6628bfa3d90f1a72`  
		Last Modified: Thu, 13 Feb 2025 00:31:55 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb7179cf0a37820dba73bc47b3738547cad87da97940398cb86c1723117f401`  
		Last Modified: Thu, 13 Feb 2025 00:32:10 GMT  
		Size: 355.1 MB (355106409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b7babf320c6bc5457dee1c060552154ad1ba5f898d97777b84684b952bb085`  
		Last Modified: Thu, 13 Feb 2025 00:31:56 GMT  
		Size: 3.9 MB (3874762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb61a1cc81f9c3bfed8a32be7b64adc61c049c3191d8f1b0cd0bf46287614f05`  
		Last Modified: Thu, 13 Feb 2025 00:31:56 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
