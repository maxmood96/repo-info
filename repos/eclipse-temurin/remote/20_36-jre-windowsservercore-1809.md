## `eclipse-temurin:20_36-jre-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:5d90b1755d385f329468db514a94ed5f0b5174a8820796703fb2efa27587cf20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4131; amd64

### `eclipse-temurin:20_36-jre-windowsservercore-1809` - windows version 10.0.17763.4131; amd64

```console
$ docker pull eclipse-temurin@sha256:7648168dae4ea87d582fe7db6940644df35ec41a9e18e296a1abc540ad78cf58
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2095449073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6213625cf259cfaab1732ad7b292bb499bdb1801dea691f08c636c334e77e74`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Sat, 11 Mar 2023 10:37:22 GMT
RUN Install update 10.0.17763.4131
# Thu, 16 Mar 2023 00:41:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 27 Mar 2023 20:21:21 GMT
ENV JAVA_VERSION=jdk-20+36
# Mon, 27 Mar 2023 20:29:40 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20%2B36/OpenJDK20U-jre_x64_windows_hotspot_20_36.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20%2B36/OpenJDK20U-jre_x64_windows_hotspot_20_36.msi ;     Write-Host ('Verifying sha256 (b8e923bcd2f03fa84887c14fec0c573b843c6d4b9671c3044e41706c579b4547) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'b8e923bcd2f03fa84887c14fec0c573b843c6d4b9671c3044e41706c579b4547') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-20' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Mon, 27 Mar 2023 20:30:55 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92048040b3b13af10f8287baabaddbb2759dfc77b1fb43f89b38b3275467f93`  
		Last Modified: Thu, 16 Mar 2023 01:42:29 GMT  
		Size: 305.6 MB (305565048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8e4e0836091bdd33e8adb56d1e13b8096550727a20534e2a2ab9298c86fa09`  
		Last Modified: Thu, 16 Mar 2023 01:41:16 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7ad651795c7799acc4387c75cb499ba4617d2e60a88dd40e6202441c878f52`  
		Last Modified: Mon, 27 Mar 2023 20:37:44 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4268e7a2eab4ca37815702da2225ea0a5d5edaf011c6c8eea3bad35b98b34b7`  
		Last Modified: Mon, 27 Mar 2023 20:39:33 GMT  
		Size: 78.6 MB (78551487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4cc7cc2c3d0f0d9bcd1eb1eec54c3edaa3814cb3158a1e07a72358a9285b261`  
		Last Modified: Mon, 27 Mar 2023 20:39:23 GMT  
		Size: 3.4 MB (3385761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
