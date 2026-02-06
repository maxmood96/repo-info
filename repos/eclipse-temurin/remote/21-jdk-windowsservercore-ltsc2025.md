## `eclipse-temurin:21-jdk-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:b336644476289837164d8dc5e2bc6b98a46aa13b0bad7f4004b5219e206f977c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `eclipse-temurin:21-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull eclipse-temurin@sha256:5e27dc2d2b43d122bd47324b06fa420adab3f69dcea6bd5486b126c6d4608d14
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1876833904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff81cd15cc676e642853f95d903e6cbb625df2b60309943bcbb36c22f1f06a8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Thu, 05 Feb 2026 22:17:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Feb 2026 22:17:02 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Thu, 05 Feb 2026 22:17:57 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_windows_hotspot_21.0.10_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_windows_hotspot_21.0.10_7.msi ;     Write-Host ('Verifying sha256 (6be8643444ec20758a34ddb1231e998ac77e72f661a0d5525a8ac3e078bcbcb0) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '6be8643444ec20758a34ddb1231e998ac77e72f661a0d5525a8ac3e078bcbcb0') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 05 Feb 2026 22:18:04 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 05 Feb 2026 22:18:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4bd51021594de608b9c2ba92f1c09460e19eceb50da801338bb4b595b24bf85`  
		Last Modified: Thu, 05 Feb 2026 22:18:09 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67a42270a134965def014a16d0f3ab2585a1f687bc5c01a2437c561f63d91d9e`  
		Last Modified: Thu, 05 Feb 2026 22:18:09 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0abd8d136eea0557bb4dd335b32e26802356cb5cd2e5c6544e644f1a7ab86174`  
		Last Modified: Thu, 05 Feb 2026 22:18:29 GMT  
		Size: 380.7 MB (380688744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a58bc174a90232ac5583ebdbda6625f8841891c8d0fc14dbb9c7476abdcd2e`  
		Last Modified: Thu, 05 Feb 2026 22:18:09 GMT  
		Size: 380.9 KB (380914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c00efa4a82dc46e2f608f263e2ba529982724ee4297f572927b6e5368ec0e9`  
		Last Modified: Thu, 05 Feb 2026 22:18:08 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
