## `eclipse-temurin:17-jdk-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:591f72b30b7769fee7e1451bfa9e9ad6612d88305621db089907ce4fb62e40a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:17-jdk-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull eclipse-temurin@sha256:d6764f06fd0ff83fdce49915e244b7881a24dcd7cd046395c49e1898f3cd82a3
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2481159286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1f0c88ed555512e00ac9eef2490b1798e452bb025aa7d51ef11f69a88cca92`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Fri, 31 Jan 2025 01:29:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Jan 2025 01:29:31 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Fri, 31 Jan 2025 01:31:39 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_windows_hotspot_17.0.14_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_windows_hotspot_17.0.14_7.msi ;     Write-Host ('Verifying sha256 (021589cc7d85392b24c3992331d84b25f0b1c1e6603dae07594abb97105fa67f) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '021589cc7d85392b24c3992331d84b25f0b1c1e6603dae07594abb97105fa67f') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 31 Jan 2025 01:31:56 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Fri, 31 Jan 2025 01:31:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b946cd74c9a810d5107c44fdc6dc027d348b46ce17e21634cb634442b7daff0`  
		Last Modified: Fri, 31 Jan 2025 01:31:59 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06bc0d05434abe924ce1e487f7bc721d555408bcec13c92c5f8e65b41977887a`  
		Last Modified: Fri, 31 Jan 2025 01:31:59 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e828083471083b89dc8ce2cd96befebb588f0c630fed486df71096b96c3434`  
		Last Modified: Fri, 31 Jan 2025 01:32:13 GMT  
		Size: 355.1 MB (355098471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2088c123e55dc397e829f612449814b5549dd3958ea20015875cb4e99cb695e8`  
		Last Modified: Fri, 31 Jan 2025 01:32:00 GMT  
		Size: 3.8 MB (3844749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921e1b37dc294e9c6db7b2f567d24f12a9f2001964f6f628ed640ebf6e7cef58`  
		Last Modified: Fri, 31 Jan 2025 01:31:59 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
