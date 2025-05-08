## `eclipse-temurin:21-jdk-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:f3666c8d5a7cb8d15e3d463e0e3d82d77f577d730fe0d8b413fb26afe02971c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `eclipse-temurin:21-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull eclipse-temurin@sha256:02ccf6d5ffdfdfae2a3d651fcfcb5cb820d92f96c27bbfe6e6cc4c7c43e4912f
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2654352239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:261fb5f15df0c9c92a7b50fa78390a8be1fc75d7af46e49422b114263ec18fd4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Wed, 23 Apr 2025 16:45:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 23 Apr 2025 16:45:19 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 23 Apr 2025 16:45:51 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_x64_windows_hotspot_21.0.7_6.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_x64_windows_hotspot_21.0.7_6.msi ;     Write-Host ('Verifying sha256 (168e3c710448dbdd7e6fe2463b867339a72be11a7c8615d72d19fb26572d3619) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '168e3c710448dbdd7e6fe2463b867339a72be11a7c8615d72d19fb26572d3619') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 23 Apr 2025 16:46:00 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 23 Apr 2025 16:46:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6ee194dfee460cc53e0f761b7ff976c08380d6cd1e70cc50ff92cfa99d176`  
		Last Modified: Thu, 08 May 2025 17:22:47 GMT  
		Size: 811.4 MB (811390127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:349143c3663bda23aca202ffbc17bf8c01699498a4eb70d38d3b183446f757b6`  
		Last Modified: Wed, 23 Apr 2025 16:46:02 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed495a2ddd514142eeba89d966613de2e056ee7b2afb31702bbc7b4da98393f`  
		Last Modified: Wed, 23 Apr 2025 16:46:03 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50afcd92fde395076ab1352c00ed6a81c057997771a2b55c173cae427ea3af8e`  
		Last Modified: Wed, 23 Apr 2025 16:46:18 GMT  
		Size: 380.4 MB (380392946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39cfb6ad1a7df91be0b4f25d0180ee11436869af36029fe1b5f8ab37db9d13da`  
		Last Modified: Wed, 23 Apr 2025 16:46:03 GMT  
		Size: 372.9 KB (372900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1d125bd330b9f24c1c43f2f54b95e71b91144d292a42c0abce1bcbaab68fd8`  
		Last Modified: Wed, 23 Apr 2025 16:46:02 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
