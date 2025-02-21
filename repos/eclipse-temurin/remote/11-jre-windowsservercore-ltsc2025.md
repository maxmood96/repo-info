## `eclipse-temurin:11-jre-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:186781b0b7c6a3bb4bfc0ee25d8c6ef15b86077a2455781c2e7af0ba0485af0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `eclipse-temurin:11-jre-windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull eclipse-temurin@sha256:234c6c1c7d5a67a753430b4d6cba10d87fb8bf13f542a3119b805ce38c416d03
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2575679696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8533262d566b5dd2959752aa46d0006d23a3ea8e63d3059b5ffd2f71549cc1fd`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Fri, 31 Jan 2025 02:16:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Jan 2025 02:16:46 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Fri, 31 Jan 2025 02:17:01 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_windows_hotspot_11.0.26_4.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_windows_hotspot_11.0.26_4.msi ;     Write-Host ('Verifying sha256 (5e1e515f2625ab6c4bdc95a6a0f0928b3ace6034a60d811da3d701ebfaeaccf1) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '5e1e515f2625ab6c4bdc95a6a0f0928b3ace6034a60d811da3d701ebfaeaccf1') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 31 Jan 2025 02:17:09 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83aab61b9dc99dc2260753e3f19dd8bb3c1098062e6b0c398a8c67cd04d37566`  
		Last Modified: Fri, 31 Jan 2025 02:17:13 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550bb9522c20badd8ca2ad2cfe5356617b07def897ad884de65f564706bc5307`  
		Last Modified: Fri, 31 Jan 2025 02:17:13 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a99a7ce0a24e05733abb76507834224553ab7618d7b605f985712c0d3f47ca`  
		Last Modified: Fri, 31 Jan 2025 02:17:20 GMT  
		Size: 75.0 MB (75006059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340c18e552fac0c15a157965c7379d7ae9dc077dd49ec5394718edab4206fc61`  
		Last Modified: Fri, 31 Jan 2025 02:17:14 GMT  
		Size: 393.5 KB (393492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
