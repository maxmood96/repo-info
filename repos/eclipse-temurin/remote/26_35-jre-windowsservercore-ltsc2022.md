## `eclipse-temurin:26_35-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:c16aea650ca49bf1a199235a9f9b8708dc0ecab04288047429ef97d55e4a494b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `eclipse-temurin:26_35-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull eclipse-temurin@sha256:e7dde16cd7da674c52399ac9830c552ba882603dddab3854738cfaa22e4b33e7
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2174674842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4655780b17f92446e93c44829938de675965badd2a9012df9e8a39dd1650ea3f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 14 Apr 2026 21:03:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 21:16:11 GMT
ENV JAVA_VERSION=jdk-26+35
# Tue, 14 Apr 2026 21:16:32 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_x64_windows_hotspot_26_35.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_x64_windows_hotspot_26_35.msi ;     Write-Host ('Verifying sha256 (891d4a89535cb0d0451428aa9ce6d87908cc147113b38eef896de6a429052507) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '891d4a89535cb0d0451428aa9ce6d87908cc147113b38eef896de6a429052507') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-26' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 14 Apr 2026 21:16:39 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a087a5c83078249a158dcc895211db8e8e14cc1e3497a33a95a3233f9a4c66ff`  
		Last Modified: Tue, 14 Apr 2026 21:06:52 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf58d8fb7a6f622739459a9ec7f1db26d89ed1c2b71dc3d5a14744a159da337`  
		Last Modified: Tue, 14 Apr 2026 21:16:42 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0308964db127a348ca500fdeb904cfa93062ba3f659652805a2178bfddd8478`  
		Last Modified: Tue, 14 Apr 2026 21:16:53 GMT  
		Size: 104.1 MB (104108566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be60df1443eae4107ed0315d0ae62c356ff8f86c432a47fa50ca84d59567710`  
		Last Modified: Tue, 14 Apr 2026 21:16:43 GMT  
		Size: 352.4 KB (352359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
