## `eclipse-temurin:21-jre-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:3837eae4162fc6d482106bf497029a6603a2c074f35049ada9f81c0341dc8e5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `eclipse-temurin:21-jre-windowsservercore` - windows version 10.0.26100.32690; amd64

```console
$ docker pull eclipse-temurin@sha256:de2d679c4ad62bfba475cd58522ced21aeebe6bfce0abae066297cd21d1f4390
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2214345797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f1cd4ab43da9374971d856e1e1600975dfffee44acbf320e0797873510e79e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Fri, 08 May 2026 00:02:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 08 May 2026 00:02:43 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Fri, 08 May 2026 00:04:07 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_windows_hotspot_21.0.11_10.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_windows_hotspot_21.0.11_10.msi ;     Write-Host ('Verifying sha256 (570b2b7f4d39638afe416e14285e08f27fd14995e0716dcbc07f936a5b91868a) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '570b2b7f4d39638afe416e14285e08f27fd14995e0716dcbc07f936a5b91868a') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 08 May 2026 00:04:15 GMT
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
	-	`sha256:07202675e8b332280c1ce8ab9a684fe68ce666346e61adb08987f2702f662007`  
		Last Modified: Fri, 08 May 2026 00:04:19 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fdddc0cd61f3bac394ae65df9287b1264e95862922843c8d0b68310bcf2d0db`  
		Last Modified: Fri, 08 May 2026 00:04:19 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac65f8d76530794a738dc69aefe3fcb9b606420c6d9abdbaa13be295ea708bb`  
		Last Modified: Fri, 08 May 2026 00:04:27 GMT  
		Size: 84.0 MB (84007182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7b0962cc1a518222ede2f04136149e14c32b8255227f62f0e201adfc407240`  
		Last Modified: Fri, 08 May 2026 00:04:19 GMT  
		Size: 350.0 KB (350006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-windowsservercore` - windows version 10.0.20348.5020; amd64

```console
$ docker pull eclipse-temurin@sha256:cfa31dbc66877ab6e882d7b1b20240e23697e1668124681221a3018ec6126d67
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2154557655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a509037cc0cecba3496e233475be3ddeb0b615f732ba11518fbec6083513e40`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Thu, 07 May 2026 23:58:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 08 May 2026 00:16:03 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Fri, 08 May 2026 00:17:38 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_windows_hotspot_21.0.11_10.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_windows_hotspot_21.0.11_10.msi ;     Write-Host ('Verifying sha256 (570b2b7f4d39638afe416e14285e08f27fd14995e0716dcbc07f936a5b91868a) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '570b2b7f4d39638afe416e14285e08f27fd14995e0716dcbc07f936a5b91868a') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 08 May 2026 00:17:46 GMT
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
	-	`sha256:d5fde2c0bc0fe84baca4fbfe521549b09e91916c26f6276a0e25f855a36a095c`  
		Last Modified: Fri, 08 May 2026 00:00:22 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca823d12cb67a12b0a88ef3dfe55f00ed1395323ef55bdba27c4a88173fc671`  
		Last Modified: Fri, 08 May 2026 00:16:40 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56acd87b8452f6a4a59daa88ec316e3f171ae5dd4eac5fb2e3e4e15083e62f6c`  
		Last Modified: Fri, 08 May 2026 00:17:59 GMT  
		Size: 84.0 MB (83977373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5c64ac1ed34e5b7058ed9962d82c3debde3fc9911918e5ea2d0377d2ea674e`  
		Last Modified: Fri, 08 May 2026 00:17:50 GMT  
		Size: 366.4 KB (366426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
