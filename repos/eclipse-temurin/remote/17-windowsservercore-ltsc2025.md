## `eclipse-temurin:17-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:9e1daf5b9146661d9c99e79d125b768a10e68128b11bc162806c3f5a4ce6a69d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3781; amd64

### `eclipse-temurin:17-windowsservercore-ltsc2025` - windows version 10.0.26100.3781; amd64

```console
$ docker pull eclipse-temurin@sha256:029008be8bf38f667e38dcd4ce697568cb42c2e6bab9d6680557657de4878e9a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 GB (3750844937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70a37c0dc9a4fe34ade5a376c7f638886902cc5194caee79548bebf997a72fdc`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Tue, 15 Apr 2025 10:03:37 GMT
RUN Install update 10.0.26100.3781
# Wed, 23 Apr 2025 16:36:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 23 Apr 2025 16:36:38 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 16:37:04 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_x64_windows_hotspot_17.0.15_6.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_x64_windows_hotspot_17.0.15_6.msi ;     Write-Host ('Verifying sha256 (f3cbf808924aa62280475821c1ec9c0b671f6f2c542408a6a21f6b84957daabd) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'f3cbf808924aa62280475821c1ec9c0b671f6f2c542408a6a21f6b84957daabd') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 23 Apr 2025 16:37:12 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 23 Apr 2025 16:37:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a55b9bd12cfb5d81d64963683e6d5d0ba9423233c85140eff135128a64f7ee`  
		Last Modified: Thu, 08 May 2025 17:36:06 GMT  
		Size: 1.2 GB (1179854238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba78d8df707fa24b2a4486e36b8c74047701e28b1383da552069b5dbe57c8b34`  
		Last Modified: Fri, 09 May 2025 12:03:13 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77cdcddf02680b61a5407ecc43137a431ab90f297b1abfe2d9b50382d558359`  
		Last Modified: Fri, 09 May 2025 12:03:13 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba78a90779c25dfd0329f15811e70a8c7f1e5b274bef69e688ef8117d990f39`  
		Last Modified: Wed, 23 Apr 2025 16:37:35 GMT  
		Size: 355.3 MB (355293063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bceaea5bd0d39df9a5184dd8b95eacfe9762f423bbd5cad0202bbea33d5336e8`  
		Last Modified: Fri, 09 May 2025 12:03:14 GMT  
		Size: 386.6 KB (386606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3abd3c1d7583a0d113cb35dbb2def20b1eb7ec389cb1ede1e15cb20c25eb4bfc`  
		Last Modified: Fri, 09 May 2025 12:03:13 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
