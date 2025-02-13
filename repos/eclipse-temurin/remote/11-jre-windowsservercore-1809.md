## `eclipse-temurin:11-jre-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:a0a59173ecda65c896b8b7c1bcb02f047e9d441c0b0f5157f4b5bc576373bb3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:11-jre-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull eclipse-temurin@sha256:8b6d3126a143a7ac6e41d55d7394d3638c3051073ec064aa8fe6f37179aebc7b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2197502565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:decd8b0165fb044127c986c7d62b95262f2308b0bc9ab9db7db663e047ab7921`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Fri, 31 Jan 2025 02:12:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Jan 2025 02:12:29 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Fri, 31 Jan 2025 02:14:32 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_windows_hotspot_11.0.26_4.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_windows_hotspot_11.0.26_4.msi ;     Write-Host ('Verifying sha256 (5e1e515f2625ab6c4bdc95a6a0f0928b3ace6034a60d811da3d701ebfaeaccf1) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '5e1e515f2625ab6c4bdc95a6a0f0928b3ace6034a60d811da3d701ebfaeaccf1') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 31 Jan 2025 02:14:43 GMT
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
	-	`sha256:28e0fd9bdd8f1cf6abbf335c07e008662aa693dc363700ee5921a1cec984eeaf`  
		Last Modified: Sun, 09 Feb 2025 12:01:37 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7743386ad5a0db71c2041930a29cb490b3f135c1d52a3177b30f7ae693e90b5f`  
		Last Modified: Sun, 09 Feb 2025 12:01:38 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d76bdd4e03e84060c951af5477e94ccd48aac5b3f99f2c251dd3cf03cf74a6`  
		Last Modified: Mon, 10 Feb 2025 13:56:17 GMT  
		Size: 75.0 MB (74973697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68656dc11b4390da25337000473553cc695c49b013a9e6eb91d38743fc85a86e`  
		Last Modified: Sun, 09 Feb 2025 12:01:42 GMT  
		Size: 314.1 KB (314080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
