## `eclipse-temurin:17-jre-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:7c935313d2be06c4d12ccd423c68d1f31f0cddcc3d5a064bb37cf65cfd63fecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `eclipse-temurin:17-jre-windowsservercore-ltsc2025` - windows version 10.0.26100.6905; amd64

```console
$ docker pull eclipse-temurin@sha256:2156f014ee77e5d6d4b44a9857d189d7dd6f5cde616279d8e13c34066902094e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3295690067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8048ae1cfb5fa1281c2658a4d53a7e3b73684cf2184de4a56b36d03fe826c7b5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 24 Oct 2025 18:13:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:22:57 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 24 Oct 2025 18:23:20 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_windows_hotspot_17.0.16_8.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_windows_hotspot_17.0.16_8.msi ;     Write-Host ('Verifying sha256 (9937d754d7157dcdb7ec70a83a5e6238ce093c71316435b4dd07ae38880980d2) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '9937d754d7157dcdb7ec70a83a5e6238ce093c71316435b4dd07ae38880980d2') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 24 Oct 2025 18:23:25 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9235cc3c3cb68485c33877f779011c5a8c97c24f91de0e5999d9885837e759`  
		Last Modified: Fri, 24 Oct 2025 18:22:38 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7318e56c183c8fed833db1726ad9840b26897df97d1280ebbde15f294ad5ccd1`  
		Last Modified: Fri, 24 Oct 2025 18:23:44 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf0742fe106bb43b73b782aa7590a40a7c9462fe8c81206c9cdfbde4d451075`  
		Last Modified: Fri, 24 Oct 2025 18:23:53 GMT  
		Size: 75.0 MB (75010804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a3b2527e67f1fca0134a9e0969a648f9d07c28797e3447ac21e528344b7860`  
		Last Modified: Fri, 24 Oct 2025 18:23:44 GMT  
		Size: 329.6 KB (329630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
