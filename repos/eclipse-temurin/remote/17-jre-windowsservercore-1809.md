## `eclipse-temurin:17-jre-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:bb3a619014cb2e0b5147851873bd8d772458ec04293f3c40ac21c8bef31216a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2366; amd64

### `eclipse-temurin:17-jre-windowsservercore-1809` - windows version 10.0.17763.2366; amd64

```console
$ docker pull eclipse-temurin@sha256:efc9da7b021b2790eefc7a333c08d333b8b6643beccb1be52578642039f7b8ef
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2786026200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c690a81aa07248ddfc3a96cda22492a232cfd522cd4b275e4016a6fb10856e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 07 Dec 2021 04:56:01 GMT
RUN Install update 1809-amd64
# Fri, 17 Dec 2021 23:26:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 18 Dec 2021 05:55:22 GMT
ENV JAVA_VERSION=jdk-17.0.1+12
# Tue, 21 Dec 2021 18:21:21 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jre_x64_windows_hotspot_17.0.1_12.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jre_x64_windows_hotspot_17.0.1_12.msi ;     Write-Host ('Verifying sha256 (f1580b6aa2071448798d5f5e3c229fc150cb5bc4e650c365121be9afdf4c313b) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'f1580b6aa2071448798d5f5e3c229fc150cb5bc4e650c365121be9afdf4c313b') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 21 Dec 2021 18:22:20 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5ee7a7ea9cf22f75886179907a41810a992e21f3d0c57cc10d2147ce9237701c`  
		Size: 990.3 MB (990271574 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:31b2acce136e44984ba36d64717a6a67fbf1a98ed7ffcf0a14df848c1502a345`  
		Last Modified: Fri, 17 Dec 2021 23:47:14 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f2f95f84871a76cc9cb58e4f71d6d7ea4f97408c3d29cf1f855c5fd29d49dc4`  
		Last Modified: Sat, 18 Dec 2021 06:39:23 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:477da5d17a15b751671fff84d8f1e1135ff8097b5ea0f9e075fa371794474c4d`  
		Last Modified: Tue, 21 Dec 2021 18:31:01 GMT  
		Size: 74.1 MB (74135842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa43dc5a326e13df587e30eeb05e793d74461910e1d8bccd451194295145c5cd`  
		Last Modified: Tue, 21 Dec 2021 18:30:50 GMT  
		Size: 3.3 MB (3283067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
