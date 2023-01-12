## `eclipse-temurin:11-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:55ac4409b6b502a747e455014e4c628c9bea69c28fc6f872924da4da0e3da9e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3887; amd64

### `eclipse-temurin:11-windowsservercore-1809` - windows version 10.0.17763.3887; amd64

```console
$ docker pull eclipse-temurin@sha256:be6df383ea443f7c636f568809c8349b66e13610bbeee931b1dff7ae83c6e987
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2074540804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a678c2a6fa8713d515b6a658dc0c2acbb62217828dca9c7020977a728e3790d8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 01:53:24 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Thu, 12 Jan 2023 01:54:54 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jdk_x64_windows_hotspot_11.0.17_8.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jdk_x64_windows_hotspot_11.0.17_8.msi ;     Write-Host ('Verifying sha256 (9b74536f2475b67e53c83ecf41f80ac9f1ba29cef91c6e261e10d1223da42d69) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '9b74536f2475b67e53c83ecf41f80ac9f1ba29cef91c6e261e10d1223da42d69') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 12 Jan 2023 01:55:33 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 12 Jan 2023 01:55:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691d210e0841eeceff800f3b441be6db4bc689728f1bb771ce88f839d06f57d0`  
		Last Modified: Thu, 12 Jan 2023 02:34:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a81eed0c1ea0654021b1fc65378a634985f8dea1c16244280c90f0440f1aa2`  
		Last Modified: Thu, 12 Jan 2023 02:42:28 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eda7402d31d25274ff2542b74ab0d026e1a2a540651f12b8f347655128e2d9e`  
		Last Modified: Thu, 12 Jan 2023 02:43:02 GMT  
		Size: 366.3 MB (366265845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:839a18492c4574ecd375b82aea953dc18b5f30e7910646a2fcd898291ebf54ab`  
		Last Modified: Thu, 12 Jan 2023 02:42:28 GMT  
		Size: 326.8 KB (326794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ce7a29a338b7e388fcabf9d600cdbb5c4e8b4ac60cb4dd388f183ca2316838`  
		Last Modified: Thu, 12 Jan 2023 02:42:28 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
