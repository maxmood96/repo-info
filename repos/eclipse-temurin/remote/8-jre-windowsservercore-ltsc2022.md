## `eclipse-temurin:8-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:813ebdbe53fe0714c244abb26e257ab33af92192fb78d30b0fc105249086914d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.887; amd64

### `eclipse-temurin:8-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.887; amd64

```console
$ docker pull eclipse-temurin@sha256:94eff190e81a1cacb9da034f290ff3f1d526d20aa8dc5c1a342a04a4ba1a1054
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2388708480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dba189c27acd09003d91344275b2ece14659f7c61493d1f524356f0388049040`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Sat, 06 Aug 2022 02:59:35 GMT
RUN Install update 10.0.20348.887
# Wed, 10 Aug 2022 12:11:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Aug 2022 15:52:57 GMT
ENV JAVA_VERSION=jdk8u342-b07.1
# Wed, 10 Aug 2022 15:58:31 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u342-b07.1/OpenJDK8U-jre_x64_windows_hotspot_8u342b07.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u342-b07.1/OpenJDK8U-jre_x64_windows_hotspot_8u342b07.msi ;     Write-Host ('Verifying sha256 (70e90ac93841ae85a966fb404343f89bf6518eac1e892eda5100da4d4433a95e) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '70e90ac93841ae85a966fb404343f89bf6518eac1e892eda5100da4d4433a95e') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 10 Aug 2022 15:58:49 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:97b25a378238b615dc51216c4d87ce17fd3cc3dca9db458e8705d1a4c17e3bb7`  
		Size: 880.0 MB (880025531 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4a5e3787c778295a5877e0381020b02273a985f7db2dd483ddff586869546e4c`  
		Last Modified: Wed, 10 Aug 2022 12:42:34 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b70c09324a60c2649aec49e94028e1aed2747bf749e16792d0f7361060c34a7`  
		Last Modified: Wed, 10 Aug 2022 16:37:33 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1ff0dda894f5c4d592e2eef5fd7efcc8ce86a2dab88918514500a16c7fbb5c`  
		Last Modified: Wed, 10 Aug 2022 16:39:11 GMT  
		Size: 71.2 MB (71246431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f9aeb56d786d8e997051cbdcfe9f17b41473024c3a7676b83b39606cf28d636`  
		Last Modified: Wed, 10 Aug 2022 16:39:02 GMT  
		Size: 570.1 KB (570062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
