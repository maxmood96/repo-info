## `eclipse-temurin:24-jdk-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:6b6b57ba98c8e6b137cbeb0eb3db12aa96f16df5d60474a4a07fa59286c93305
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3932; amd64

### `eclipse-temurin:24-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.3932; amd64

```console
$ docker pull eclipse-temurin@sha256:6ca8a93c635bcfb35045e89bdd91149cad63537195aefcbb0b45809cca44f5f5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2533529543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d54189b8bff1d35810fe97e65bed7c451258e7e4fa6f1bb804ff88861286c9a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 05 Jul 2025 05:31:06 GMT
RUN Install update 10.0.20348.3932
# Wed, 09 Jul 2025 18:06:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jul 2025 18:06:35 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Wed, 09 Jul 2025 18:06:56 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_x64_windows_hotspot_24.0.1_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_x64_windows_hotspot_24.0.1_9.msi ;     Write-Host ('Verifying sha256 (c820fd88f666dbb56109095a7a82ce82ebc0aedb0a0d6d1dd9f75fe2b7ac0eb0) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'c820fd88f666dbb56109095a7a82ce82ebc0aedb0a0d6d1dd9f75fe2b7ac0eb0') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-24' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 09 Jul 2025 18:07:03 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 09 Jul 2025 18:07:04 GMT
CMD ["jshell"]
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
	-	`sha256:f6bcef584a43fa50739471a8cee05d8a4c8d21ffacc2fd8e083268179e01444b`  
		Last Modified: Wed, 09 Jul 2025 19:08:17 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c7e44830d0dd39143448fe5debaf79f8b175ba37c476ba5c35140166908c21`  
		Last Modified: Wed, 09 Jul 2025 19:08:17 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6ad2afbd3b595eb207b95a966c630bd0278388b5a1c0a01da123b36ddf12ac`  
		Last Modified: Wed, 09 Jul 2025 19:08:38 GMT  
		Size: 252.6 MB (252554819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1554660613efc3e20e57b29c2c82d68b307c7c5108a2a3aea884f298cffe9b8e`  
		Last Modified: Wed, 09 Jul 2025 19:08:17 GMT  
		Size: 367.4 KB (367389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:542e08039f9fa5f3edeeb9fa12c1856067959577faab94ce3de5027c39367ea5`  
		Last Modified: Wed, 09 Jul 2025 19:08:18 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
