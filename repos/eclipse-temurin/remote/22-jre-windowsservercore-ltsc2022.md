## `eclipse-temurin:22-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:d51896cf1f0f42a6ca1235efb035680afe21e5a372cdf77d01a28591a7c334f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `eclipse-temurin:22-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull eclipse-temurin@sha256:55782d3cad0269e3c31280fbddce683b3149adb5f2dd91941a569bf99ffcca03
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1545177455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef27667adf3e6292ebec77116106bc0479499d015253048945f52f6cd96935e1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 11 Sep 2024 00:35:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 00:59:58 GMT
ENV JAVA_VERSION=jdk-22.0.2+9
# Wed, 11 Sep 2024 01:03:53 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jre_x64_windows_hotspot_22.0.2_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jre_x64_windows_hotspot_22.0.2_9.msi ;     Write-Host ('Verifying sha256 (976ca7a664831ac76cd956ce525e6c86ddcadb70c0bc29a3754c55c991955cb7) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '976ca7a664831ac76cd956ce525e6c86ddcadb70c0bc29a3754c55c991955cb7') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-22' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 11 Sep 2024 01:04:10 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e0ff9a79ca5aec0b3e3be0c49c873a237847a9d74342acad1818e3f10647107`  
		Last Modified: Wed, 11 Sep 2024 01:13:29 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d58ba21cab3ac9d3120e7a871ec58aa53c0b919591d4e76d24f776882ac1ef8`  
		Last Modified: Wed, 11 Sep 2024 01:30:40 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91454a31bcad861d7c0b038ca1c91dfb77d12f67a02ded1eb15e2ef1f404dc51`  
		Last Modified: Wed, 11 Sep 2024 01:32:27 GMT  
		Size: 82.7 MB (82705862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c99c7f90cc430bbff5c0d642aceef0ac0d920908862f01a72ba4b5328702ce91`  
		Last Modified: Wed, 11 Sep 2024 01:32:17 GMT  
		Size: 276.3 KB (276348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
