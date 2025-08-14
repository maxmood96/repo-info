## `eclipse-temurin:17-jdk-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:b0b1f01f39a4623205eaf6acc01febaf42acc48fcd62b5895d6a4427e26196ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `eclipse-temurin:17-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull eclipse-temurin@sha256:e3cad525f9a3ebd9de18a6dae9426754ed9c1469c3a1e1642afbc6d519892161
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2637261152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c8b2ad65f5784054aa6874372ac91da678fada32d1299b733ba7a81de50668a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:32:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:32:17 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Tue, 12 Aug 2025 20:32:45 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_windows_hotspot_17.0.16_8.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_windows_hotspot_17.0.16_8.msi ;     Write-Host ('Verifying sha256 (1c3701f074d75036650731bcf6b08d69b1e3567bfa853f0ddd7aaba44da5b595) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '1c3701f074d75036650731bcf6b08d69b1e3567bfa853f0ddd7aaba44da5b595') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 12 Aug 2025 20:32:53 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 12 Aug 2025 20:32:54 GMT
CMD ["jshell"]
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
	-	`sha256:3ef125f5e67f9b7e59d2eff05c7432c9c7806a1c151183caaf8c78e229ed68ef`  
		Last Modified: Tue, 12 Aug 2025 20:34:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1299d9da7165b4e124d638c8cd176002ef12d5291d972ba89243f092d2283e`  
		Last Modified: Tue, 12 Aug 2025 20:34:46 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f897b9cc2b87ff59a66c62e0f2a3c7df9eefcc0923d20b28619e7cf8a588bc3c`  
		Last Modified: Tue, 12 Aug 2025 20:45:29 GMT  
		Size: 355.2 MB (355217735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a081417b3b317d60c46b33691dec416fbbee9a31497e9c86d0a7f0b24dae22e4`  
		Last Modified: Tue, 12 Aug 2025 20:34:46 GMT  
		Size: 347.5 KB (347543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ccd7d249874131b0584ed213841c0a6bd66f76200264cae76637a74e48ccb1`  
		Last Modified: Tue, 12 Aug 2025 20:34:48 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
