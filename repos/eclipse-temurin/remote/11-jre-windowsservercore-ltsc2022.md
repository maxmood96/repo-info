## `eclipse-temurin:11-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:5b915684b9bb9bcce1c18e179f016cf35a738f1b60acd98d97234da8d4f370f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1607; amd64

### `eclipse-temurin:11-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.1607; amd64

```console
$ docker pull eclipse-temurin@sha256:6d2555c418d121f7f3425f5143711f0e57da789a32412ac51b8a6d4f5b10fd00
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1789057054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf06e2d4515a3d7228c936477ac5f7fc71273b927dd9e8dcc7aae3bce70e4f5d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Fri, 10 Mar 2023 06:37:36 GMT
RUN Install update 10.0.20348.1607
# Thu, 16 Mar 2023 00:38:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Mar 2023 00:52:12 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 16 Mar 2023 01:00:06 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_windows_hotspot_11.0.18_10.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_windows_hotspot_11.0.18_10.msi ;     Write-Host ('Verifying sha256 (453ab7002d939ce44e54178fe1a83b4cf3cab6649e11c7aa7ee535feb6f0d7b6) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '453ab7002d939ce44e54178fe1a83b4cf3cab6649e11c7aa7ee535feb6f0d7b6') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 16 Mar 2023 01:00:35 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c921d7eac594f5e3ce3ef10adb8fd0f71bdbb713c4854336b995d25f89c44d42`  
		Last Modified: Thu, 16 Mar 2023 01:41:04 GMT  
		Size: 327.9 MB (327911088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bca4593035ae0e8d1b6e6eb1b053fddc6a6824b28f45f99de726d752d2c0f72`  
		Last Modified: Thu, 16 Mar 2023 01:39:50 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261e1c3fb2972d931b5850548b01c79e749653ccc48039b83c0a6cad3ff54552`  
		Last Modified: Thu, 16 Mar 2023 01:44:27 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d560bd2298644d8fc82179109a02cb529ea1d7e0baf235bdca293fa4e2b61f4`  
		Last Modified: Thu, 16 Mar 2023 01:46:48 GMT  
		Size: 74.6 MB (74561340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec109ba1f836ec6d8886853fc2fe88708016eb0377d671696e7342f502f7871b`  
		Last Modified: Thu, 16 Mar 2023 01:46:37 GMT  
		Size: 552.9 KB (552908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
