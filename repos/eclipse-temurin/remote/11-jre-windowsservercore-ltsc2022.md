## `eclipse-temurin:11-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:823fb013ce02774c5baee06fc9b3234f5593b9acc7967651f1cc1b8dc2271d21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `eclipse-temurin:11-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull eclipse-temurin@sha256:54fa622772de521d3930bbcd80ebdd91545cab518c80490ea0adc90f7b6761a8
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2355579469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff9a837c6b3e1a14ed0eee72fc1de7b4bd7fe31e02d859b3e6b0547da730b174`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Tue, 10 Jun 2025 21:33:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Jun 2025 21:33:03 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Tue, 10 Jun 2025 21:33:26 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_x64_windows_hotspot_11.0.27_6.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_x64_windows_hotspot_11.0.27_6.msi ;     Write-Host ('Verifying sha256 (08b8bcdf7f61f4276d90eccef6d70a4b73c25f0b4c2cdd2e6ddf15c24c087160) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '08b8bcdf7f61f4276d90eccef6d70a4b73c25f0b4c2cdd2e6ddf15c24c087160') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 10 Jun 2025 21:33:32 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f04ea0c6c5db41b580cf89fa350e3b551ed090abdaf4c3d808d37b1083950120`  
		Last Modified: Tue, 10 Jun 2025 21:35:03 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebb07608b4ea64ae08d6de11ecc8b4ebd71e70796ff6f2760d5c9dbdb6db07c`  
		Last Modified: Tue, 10 Jun 2025 21:35:03 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:105946371a1dac49446b0e47f962ef55cff60fdfab28b1a28c6716ff3ccd9b9d`  
		Last Modified: Tue, 10 Jun 2025 21:35:07 GMT  
		Size: 75.0 MB (74965646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039183fecff54104bb143b6c3b2efa8a99aba9cc93aee8674b9d7cef41a709a1`  
		Last Modified: Tue, 10 Jun 2025 21:35:04 GMT  
		Size: 359.7 KB (359676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
