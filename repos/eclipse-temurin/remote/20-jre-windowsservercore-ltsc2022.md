## `eclipse-temurin:20-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:946f6c440432e1b7e1477f2cc4c1a4eb4cf2b21ce8e1d9b418919fc69fdb677f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1970; amd64

### `eclipse-temurin:20-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.1970; amd64

```console
$ docker pull eclipse-temurin@sha256:cf10a8c8f399c9c68d71c03e565b716d9069032533c3316f3dfe5894e69ae37d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1916226589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e672839ad88fb0bb0e23114d837ef628c0436d0887153531ecb9291be03a6888`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 01 Sep 2023 00:43:48 GMT
RUN Install update 10.0.20348.1970
# Wed, 13 Sep 2023 01:35:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Sep 2023 03:05:59 GMT
ENV JAVA_VERSION=jdk-20.0.2+9
# Wed, 13 Sep 2023 03:13:42 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20.0.2%2B9/OpenJDK20U-jre_x64_windows_hotspot_20.0.2_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20.0.2%2B9/OpenJDK20U-jre_x64_windows_hotspot_20.0.2_9.msi ;     Write-Host ('Verifying sha256 (0217ba025c5ac579982a80791d4637e2b4b6afb14de522fff2b818d0203d4cea) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '0217ba025c5ac579982a80791d4637e2b4b6afb14de522fff2b818d0203d4cea') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-20' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 13 Sep 2023 03:14:13 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feca8e06011ab171ad74cda49c7c305e791965aef283d5b7c2b987dd5388e6c7`  
		Last Modified: Tue, 12 Sep 2023 18:24:42 GMT  
		Size: 448.7 MB (448675362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f40969dbf1e035a6c49e7c40b216960e3ee98ec3b76f76f9fe4498d0110bee`  
		Last Modified: Wed, 13 Sep 2023 02:15:22 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45487e7e73ad14f9d8b091ba267fce3cd52aa486492e242fab18a9edfb186d07`  
		Last Modified: Wed, 13 Sep 2023 03:43:56 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4c3134c43088af35ff14001d6cd151bdf7df88f90ba7868aaac8f261e66ca9`  
		Last Modified: Wed, 13 Sep 2023 03:46:12 GMT  
		Size: 78.7 MB (78661629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:212b1b29758cea959d60fa2c22d68e725c27bc160441d7e69858ee9968a0b81b`  
		Last Modified: Wed, 13 Sep 2023 03:46:00 GMT  
		Size: 288.1 KB (288091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
