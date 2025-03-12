## `eclipse-temurin:21-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:c4be2ca5dbf05610f5fbc91669e93ad4368901316581d4187a146e025c0d1aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `eclipse-temurin:21-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull eclipse-temurin@sha256:94a4c4f789d92bac611e183c4c2f28217d20b21d68ec237d25aad767dd230bc4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2353833869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cb008a84428f12cc6bb7e86491a618f55a52b003bf0a162948d767dfe1acc9f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Wed, 12 Mar 2025 18:51:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:51:29 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Wed, 12 Mar 2025 18:51:50 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_x64_windows_hotspot_21.0.6_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_x64_windows_hotspot_21.0.6_7.msi ;     Write-Host ('Verifying sha256 (3f511d4edbb81fdb7d044cabede018b0823b2f277103f5f47e8c72b526e9c256) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '3f511d4edbb81fdb7d044cabede018b0823b2f277103f5f47e8c72b526e9c256') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Mar 2025 18:51:56 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
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
	-	`sha256:b7bcabc150fda94cde26deb886d19a23676fe46d87481c576477292f32511177`  
		Last Modified: Wed, 12 Mar 2025 18:52:00 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e7556c3ebbbfc59d57858da777ba0c6c5c4aa80b5e93b70e7d534e03206d49`  
		Last Modified: Wed, 12 Mar 2025 18:52:00 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebae6584e2f85c66f2423afd27ba074c467bdc18c4ff7819c05828e510215f7`  
		Last Modified: Wed, 12 Mar 2025 18:52:06 GMT  
		Size: 83.5 MB (83539775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf184d44251d3b76550f6bed8811b97ffc851d8909391b4cf50037e15e311409`  
		Last Modified: Wed, 12 Mar 2025 18:52:00 GMT  
		Size: 350.3 KB (350257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
