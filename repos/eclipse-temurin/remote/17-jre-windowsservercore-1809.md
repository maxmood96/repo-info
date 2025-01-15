## `eclipse-temurin:17-jre-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:f9c8ef0593f2e6c411d494e8804d59d9d7c2d17f7ed3b72455c00dcdf8547573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:17-jre-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull eclipse-temurin@sha256:a293f50556dfb2c49b13f70bbc42c3a448b6fed0a53297a5cf1d06fd3cd60e2c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2201252854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb4cc7015cc0e7a99d5b4755e8a5e57bdc97bb811834e3449968b780738454dd`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Tue, 14 Jan 2025 23:42:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:42:42 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Tue, 14 Jan 2025 23:43:58 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_windows_hotspot_17.0.13_11.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_windows_hotspot_17.0.13_11.msi ;     Write-Host ('Verifying sha256 (457194f803be9129eaa2f0d50ac62bbd6182bf4923f91000199d936fa04e40e4) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '457194f803be9129eaa2f0d50ac62bbd6182bf4923f91000199d936fa04e40e4') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 14 Jan 2025 23:44:06 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
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
	-	`sha256:6e9598825f144a63528d22bd8cf69e6de5d11b3a0a28507d5e767e3514cbe0a3`  
		Last Modified: Tue, 14 Jan 2025 23:44:08 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d6b1f642bc66647eb23a1f5e5c4d9a4f81c73314bb5eefb00b50556561a9743`  
		Last Modified: Tue, 14 Jan 2025 23:44:08 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0211c3e361dc70a8739cea1b42a3c10afa21e3e339fcaa9847c37a112fd0cef8`  
		Last Modified: Tue, 14 Jan 2025 23:44:14 GMT  
		Size: 75.8 MB (75805792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:587a55f3e53790d554cac94c3934bb89f6046a150ec43143b62d339c53d8c0dc`  
		Last Modified: Tue, 14 Jan 2025 23:44:09 GMT  
		Size: 3.2 MB (3232275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
