## `eclipse-temurin:23-jre-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:6ef3f8f8e62e966dd9342fb34871da068fcc7f330d8ddd273f11d26631d82b9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:23-jre-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull eclipse-temurin@sha256:3be34c964b4142bad6d7989a2031bbd59b93dd26184cab3128adf0640129e15d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2209879561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b6a54120085002fb0834bf894b90a3efb8326be0a759ead54e17ea562c115d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Fri, 31 Jan 2025 01:30:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Jan 2025 01:30:31 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Fri, 31 Jan 2025 01:31:43 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_x64_windows_hotspot_23.0.2_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_x64_windows_hotspot_23.0.2_7.msi ;     Write-Host ('Verifying sha256 (07ddf8b8d004692261d0ab769a31176abd22b5203cee44317328f9113a99e486) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '07ddf8b8d004692261d0ab769a31176abd22b5203cee44317328f9113a99e486') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-23' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 31 Jan 2025 01:31:52 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 20:54:32 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220ecb0bb24b174b973fb5007cddcd591f2e577157e0146f2aac383e77952592`  
		Last Modified: Fri, 31 Jan 2025 01:31:56 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd9b5e3ce265816a3760eb5fcca2e29db5fb4093aadd07425cddd990923f3a88`  
		Last Modified: Fri, 31 Jan 2025 01:31:56 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd04f2d57b3eb8f451a2ce046693d32328d7b59361714f3550d2ee141f51454`  
		Last Modified: Fri, 31 Jan 2025 01:32:02 GMT  
		Size: 83.8 MB (83797056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67dc0a95911cdb36c2a6c3283e614420e41365ed7ece6cb610b3f26a451b6d6c`  
		Last Modified: Fri, 31 Jan 2025 01:31:57 GMT  
		Size: 3.9 MB (3867729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
