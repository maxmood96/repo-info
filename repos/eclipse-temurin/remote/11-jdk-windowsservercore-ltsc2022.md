## `eclipse-temurin:11-jdk-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:bb8bda2b4a8a0498b278a2c0c3668e4c17c762f15e7374b0e92df4426640ed35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `eclipse-temurin:11-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull eclipse-temurin@sha256:df8f850e3fe5c1e23badbda79758fcd947f1d26283bbfa040216691ccc82c573
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2639607207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:454ed45a6d3a855f34c4584d4e9139d9ad879d4bd704accbaa8870c33d365636`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Wed, 12 Mar 2025 18:56:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:56:58 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Wed, 12 Mar 2025 18:57:28 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_windows_hotspot_11.0.26_4.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_windows_hotspot_11.0.26_4.msi ;     Write-Host ('Verifying sha256 (25bc11bd05e4dad95ebefde017bd5eb29dfe8624bbd46beeca8eba4b4d77fae1) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '25bc11bd05e4dad95ebefde017bd5eb29dfe8624bbd46beeca8eba4b4d77fae1') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Mar 2025 18:57:37 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:57:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:677043d90a2ba943da579d4109dbfcce6b224542264b84e01f8659817c74a65b`  
		Last Modified: Wed, 12 Mar 2025 18:57:40 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6c67427ff447598c1f04729a9d2a4db5f27fc1f3ad1d53d78537a67370f5b9`  
		Last Modified: Wed, 12 Mar 2025 18:57:40 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc420ef2bf63d61b97b5b11c1d6dc67f4c2fab6eb59c8ca78493eacdac6fe6e`  
		Last Modified: Wed, 12 Mar 2025 18:57:56 GMT  
		Size: 369.3 MB (369302048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbaa1b878ca1a8d80e8d3a75629b31f6c318c6d9142bdd1ec3a15c87a227b09f`  
		Last Modified: Wed, 12 Mar 2025 18:57:40 GMT  
		Size: 360.1 KB (360071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:226a9c960aa60aabab57b87327bdfb6a3a4e6b87c1f70621927b01d624f589ee`  
		Last Modified: Wed, 12 Mar 2025 18:57:40 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
