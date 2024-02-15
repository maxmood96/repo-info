## `eclipse-temurin:11-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:cf67e8c8e61d82153639b9496f2cf88d646f03efa1caf331b4a858935a3e7085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2322; amd64

### `eclipse-temurin:11-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.2322; amd64

```console
$ docker pull eclipse-temurin@sha256:39b420dfea86f039584c3f80cc01bebb611d54eb1515386425a9c5995a550fcd
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1985640661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd9169685d2d7937f6065052b3de211ab64c1fe043a7b6ddae10564d0bb0eb5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Wed, 14 Feb 2024 19:36:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 19:47:18 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 14 Feb 2024 19:53:53 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_windows_hotspot_11.0.22_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_windows_hotspot_11.0.22_7.msi ;     Write-Host ('Verifying sha256 (60da81a6d02de6f253dc5ceca70822c5aabee445621abfdef6cc76cfd1db3dd9) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '60da81a6d02de6f253dc5ceca70822c5aabee445621abfdef6cc76cfd1db3dd9') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 14 Feb 2024 19:54:13 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d42cabf5bedf06720e416234beca9b72544bcc7ae0f30533edad0043aa3f12`  
		Last Modified: Wed, 14 Feb 2024 20:55:47 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37017920e0d3d53c00b84ece22edf197188167cb6ca0b6f23da5a03f641c2a8a`  
		Last Modified: Thu, 15 Feb 2024 00:08:13 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd096c8f95993db4d83fd4cef3eb060400f6967696dc56fdff3cb2d1fc17ee8`  
		Last Modified: Thu, 15 Feb 2024 00:10:11 GMT  
		Size: 74.7 MB (74701290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f6c491907b080c7af2421c3f9f56403312b2019d63a265765a296fef8a5265`  
		Last Modified: Thu, 15 Feb 2024 00:10:02 GMT  
		Size: 282.4 KB (282378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
