## `eclipse-temurin:8u482-b08-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:3c6127896884f7b640311ffdcfeaf5739d4b8e36acce087d09a5f8a0de81fecf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `eclipse-temurin:8u482-b08-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull eclipse-temurin@sha256:6a402bb1b49bfea80aebee1904dce9f09aac6f5f6b2afc7d16033c7ba63a0e4d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1934956870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d10a31d58d34aee1e66f976076dfddc1f689fbc25ccbe884787cac142e8ec135`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Tue, 10 Feb 2026 22:51:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Feb 2026 23:00:07 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 10 Feb 2026 23:00:20 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_x64_windows_hotspot_8u482b08.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_x64_windows_hotspot_8u482b08.msi ;     Write-Host ('Verifying sha256 (4e0dbdff6537f43b012e2376de59845968afc99f5901303a28a881b42d93d795) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '4e0dbdff6537f43b012e2376de59845968afc99f5901303a28a881b42d93d795') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 10 Feb 2026 23:00:25 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf582aa59c8f589f6cc77378809eabf79b679ef8c09e8e900a5ce77bf0b77e38`  
		Last Modified: Tue, 10 Feb 2026 22:55:10 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2febe100bc3ef134e143540cca5a4b86f1e880a4f4d8dd1bc5f3ec2bd1f27c5`  
		Last Modified: Tue, 10 Feb 2026 23:00:32 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83126138a16639b9b4cb4daae8c468e08de2fcabdd8fbbdf5264bbe69344e629`  
		Last Modified: Tue, 10 Feb 2026 23:00:36 GMT  
		Size: 71.9 MB (71945193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cfc0bc0e5a5f0bff50388c1d65dab516647824a40a9bb571a6a3e3e899a262e`  
		Last Modified: Tue, 10 Feb 2026 23:00:30 GMT  
		Size: 351.8 KB (351848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
