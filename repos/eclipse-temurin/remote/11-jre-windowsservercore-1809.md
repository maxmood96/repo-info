## `eclipse-temurin:11-jre-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:40e429834ac5ae0d40d6c023246dde374c6565a1539e3e09d127011202b5aa08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `eclipse-temurin:11-jre-windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull eclipse-temurin@sha256:833e1b4a8dceda9c08a108984aa867c90f6ac42d6bfe6efd8f2c7534c5d0d243
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2212225702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:564ba84c38e2a653e14eca97362a046b8e9984b3da7f85e0b35a47ae34958bcc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:36:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:36:34 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Thu, 13 Feb 2025 00:37:45 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_windows_hotspot_11.0.26_4.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_windows_hotspot_11.0.26_4.msi ;     Write-Host ('Verifying sha256 (5e1e515f2625ab6c4bdc95a6a0f0928b3ace6034a60d811da3d701ebfaeaccf1) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '5e1e515f2625ab6c4bdc95a6a0f0928b3ace6034a60d811da3d701ebfaeaccf1') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 13 Feb 2025 00:37:53 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebffc8bcd70dd0f5712b0117821e9c9bdc117b050e6d1656f1b9b91710f6414`  
		Last Modified: Thu, 13 Feb 2025 00:37:55 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d682eea9a679a9484f651457402fc64227ed6bd12a6ecc366297b28c78f6f24`  
		Last Modified: Thu, 13 Feb 2025 00:37:55 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e448f882cb55ad35b5b0c610640ea38db1a922be082811a1de8708b15e1e35`  
		Last Modified: Thu, 13 Feb 2025 00:38:00 GMT  
		Size: 75.0 MB (74975998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfca0bba5a259b1e9b2a25cabb51255dbfb686275bc8a947fa1184971ee3f2f7`  
		Last Modified: Thu, 13 Feb 2025 00:37:55 GMT  
		Size: 338.3 KB (338321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
