## `eclipse-temurin:8-jre-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:01459778976e633c8ab5265d2b587ac1754564b73dc2edc4a9b522a70b9cfc51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `eclipse-temurin:8-jre-windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull eclipse-temurin@sha256:c59988ad1fb12eb0a65c7d400272dd9e3ecfbd489407d3719a60e79bbc8a7497
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1974119501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a18447a6060c525ed4d219f60638d5cbcf215ff64cea230784c8f2d7f49db89c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Sat, 19 Oct 2024 00:55:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 19 Oct 2024 00:55:06 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Sat, 19 Oct 2024 00:57:03 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_x64_windows_hotspot_8u422b05.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_x64_windows_hotspot_8u422b05.msi ;     Write-Host ('Verifying sha256 (6a53b2e2e0eee6b238d79999e4de2fac70efc03922d48ea6d1007f50e7c11307) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '6a53b2e2e0eee6b238d79999e4de2fac70efc03922d48ea6d1007f50e7c11307') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Sat, 19 Oct 2024 00:57:14 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85744ade27454242cebd156cc09c49e9c1d08e22a8d5abe18dbda9fcb0a2e5c`  
		Last Modified: Sat, 19 Oct 2024 00:57:16 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39a5531cb7423781ea31dfc735eb9f66cd3be110def442460d34580b377a705`  
		Last Modified: Sat, 19 Oct 2024 00:57:16 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d89e15eae19727318d8774ad62637decb2a986975c4f229dac4abdae33bd5ae`  
		Last Modified: Sat, 19 Oct 2024 00:57:20 GMT  
		Size: 72.0 MB (71972473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc43f5890d9fccf75aa493c10ad99de236c92955dbe23f8d46a5b04114b7d15`  
		Last Modified: Sat, 19 Oct 2024 00:57:16 GMT  
		Size: 319.1 KB (319128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
