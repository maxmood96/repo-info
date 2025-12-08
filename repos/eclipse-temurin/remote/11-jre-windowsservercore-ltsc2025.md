## `eclipse-temurin:11-jre-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:39711ab56f6b8e0b009c9c6e877d327ea05b98960ca60a321d744e8937e2d6a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `eclipse-temurin:11-jre-windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull eclipse-temurin@sha256:8e7e6af6e450b75175a720a143aa73ea7e25ed596a027de3b71d0d3bc81c0efb
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3310735243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef3d9f99626ad0a5968ab13fa2f18f4ca7dfe2f01c0ef6db3ff0561d28f670a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:13:20 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Tue, 11 Nov 2025 19:13:41 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_x64_windows_hotspot_11.0.29_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_x64_windows_hotspot_11.0.29_7.msi ;     Write-Host ('Verifying sha256 (2113628e4feb65cc5e399c34bd1a070f8c8b931ef2899b8a7f7ac3179a3d24ce) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '2113628e4feb65cc5e399c34bd1a070f8c8b931ef2899b8a7f7ac3179a3d24ce') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 11 Nov 2025 19:13:47 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Mon, 08 Dec 2025 10:02:12 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9f07b1dfc8cfffe7adad4b99c34fdda9b3fc97e420f709121bbaab91813acd`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93831ee1e9ff4481c1fa0a1866fcae9f8250077509b9dd6548d67277abed4d3a`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14410ba737842389d631707b975510dad1699d42bd12d1827e2bff6ac90eefb7`  
		Last Modified: Tue, 11 Nov 2025 20:12:02 GMT  
		Size: 74.9 MB (74936593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146eef75ca21fc5fee647f89f213c5c1fa471117c12093a4252bac3dca667a68`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 340.4 KB (340359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
