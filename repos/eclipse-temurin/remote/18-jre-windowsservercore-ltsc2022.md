## `eclipse-temurin:18-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:387886fd47a9f8a068c722e470a42d83bf1424fa16ea205702a701c84814cb17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.825; amd64

### `eclipse-temurin:18-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.825; amd64

```console
$ docker pull eclipse-temurin@sha256:4963636b46111cee32f693db1b19b206f987c1b29b004049bc3465259d96a178
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2375392154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8cb76dc337fd62013a4eda8b99b2136ac0fc022bbb435312547803346ef0594`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Mon, 04 Jul 2022 17:46:55 GMT
RUN Install update 10.0.20348.825
# Tue, 12 Jul 2022 19:25:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Aug 2022 18:26:50 GMT
ENV JAVA_VERSION=jdk-18.0.2+9
# Tue, 02 Aug 2022 18:32:46 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jre_x64_windows_hotspot_18.0.2_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jre_x64_windows_hotspot_18.0.2_9.msi ;     Write-Host ('Verifying sha256 (5a29dbdbdfff80c24a02aa6ee239f36a1891efc4c07e80ebb238d2f9b6cdb0a8) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '5a29dbdbdfff80c24a02aa6ee239f36a1891efc4c07e80ebb238d2f9b6cdb0a8') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-18' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 02 Aug 2022 18:33:06 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e1a27cb9d4615dec325f2cbabac4ca1f65413bdbb8b440cc961df032993a9b81`  
		Size: 863.4 MB (863367943 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6452cb934201756f0ed9fb5e0cbea54a22a66412cb696ff30a1923d456e28bcf`  
		Last Modified: Tue, 12 Jul 2022 20:20:48 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc14bd69273eb440f31c9bab8b8c19bdde6f079401e43e46ed1bce8dd0b6700b`  
		Last Modified: Tue, 02 Aug 2022 18:44:13 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd9d664fe0f3fddedf27027c3966bc6f5f0ca4481e8ef8a9767f6f2a1ff66f05`  
		Last Modified: Tue, 02 Aug 2022 18:46:21 GMT  
		Size: 74.6 MB (74586526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab93292dbe7ad97048d503cb463cb95210ae8bbdd0297387f37fbe0b468b092c`  
		Last Modified: Tue, 02 Aug 2022 18:46:11 GMT  
		Size: 571.2 KB (571194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
