## `eclipse-temurin:26_35-jre-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:e5d10d41084a54055558c70561ccf4dddc84df61a99335014e0dc8b2987e93f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `eclipse-temurin:26_35-jre-windowsservercore` - windows version 10.0.26100.32690; amd64

```console
$ docker pull eclipse-temurin@sha256:8af02ebbe4f00db2b0739722b0ef3dbcf8f59e55b4409786963802215de1ad3c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2234448667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb8375c2c66be6cbc90c8d2a0442434b7ff3dad924e4b467a02a9e746a224ed`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Tue, 14 Apr 2026 21:01:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 21:11:36 GMT
ENV JAVA_VERSION=jdk-26+35
# Tue, 14 Apr 2026 21:11:52 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_x64_windows_hotspot_26_35.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_x64_windows_hotspot_26_35.msi ;     Write-Host ('Verifying sha256 (891d4a89535cb0d0451428aa9ce6d87908cc147113b38eef896de6a429052507) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '891d4a89535cb0d0451428aa9ce6d87908cc147113b38eef896de6a429052507') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-26' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 14 Apr 2026 21:11:57 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3642e4b8bb65ad3768f9f74a0dc48bb2e3294779b5d51573a234bfbe4f65324e`  
		Last Modified: Tue, 14 Apr 2026 18:48:19 GMT  
		Size: 606.9 MB (606926634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ac02bb5872fbad22e76d99d54ab9b35a1e35759bbddff4f282081ba61100d5`  
		Last Modified: Tue, 14 Apr 2026 21:02:53 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7bc7fb7e51c40b9aedec1c4be8a971ad847874a687468c909d84a018175d1eb`  
		Last Modified: Tue, 14 Apr 2026 21:12:01 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16881997c9144bf27862d3fbbe3335a61473ce81555bfda8fe8c61c437f68d4e`  
		Last Modified: Tue, 14 Apr 2026 21:12:11 GMT  
		Size: 104.1 MB (104106609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49acddadbd49470f34ba29fb4a7099bf9fafc68bb88178a0b9a80234961e54dc`  
		Last Modified: Tue, 14 Apr 2026 21:12:02 GMT  
		Size: 353.4 KB (353409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:26_35-jre-windowsservercore` - windows version 10.0.20348.5020; amd64

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
