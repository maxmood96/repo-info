## `eclipse-temurin:8-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:df53de7c8b5b6ae09b225b2e5aca0c3d388f9d15ad6f8766f89c26a4409dbea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `eclipse-temurin:8-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull eclipse-temurin@sha256:9e3a936d17c43fdd269b692b718a33c9bb0f7f649a9b3016f6175f2e43a3827c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2354671175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d311874d49098d53a2a15cb206ca0a8407e944b91cb2186cee6a275c4f4549b4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:31:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:31:38 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Tue, 12 Aug 2025 20:32:01 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_x64_windows_hotspot_8u462b08.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_x64_windows_hotspot_8u462b08.msi ;     Write-Host ('Verifying sha256 (22a64b7531443577dd70eb244c943111121180dbf20a6a867452ed6da99b556d) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '22a64b7531443577dd70eb244c943111121180dbf20a6a867452ed6da99b556d') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 12 Aug 2025 20:32:09 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aa533167bea0150a06bf787bd260a7ee257971074de998dac3dfc380fd5a666`  
		Last Modified: Tue, 12 Aug 2025 20:45:03 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c334c5e5fd008a8633f22ef9730a0e07bd55fbcd66bdf1ba85940c5204e22ef`  
		Last Modified: Tue, 12 Aug 2025 20:45:03 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d714702f01bb6e16a11ba22b6e3b07bac3eb5e6e580e9836cfe8d642398ea153`  
		Last Modified: Tue, 12 Aug 2025 20:45:13 GMT  
		Size: 72.6 MB (72628775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0be415c3ac5513c03f479fafbc34b8ef4b9d17d49e818385faa8c308cfa0a8`  
		Last Modified: Tue, 12 Aug 2025 20:45:04 GMT  
		Size: 347.9 KB (347869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
