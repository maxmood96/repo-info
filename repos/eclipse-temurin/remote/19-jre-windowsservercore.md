## `eclipse-temurin:19-jre-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:28ddafd55c7cd257580e15f9cc53528002f0ed4968bed5a9476dcede2309d9f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1607; amd64
	-	windows version 10.0.17763.4131; amd64

### `eclipse-temurin:19-jre-windowsservercore` - windows version 10.0.20348.1607; amd64

```console
$ docker pull eclipse-temurin@sha256:b29990ca4111c4f6eb3722b6e8980ee820c6c1be232ea011cd1f77d0714ab94f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1792360415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46094cbda763f676575c59905512fa0b65ffdc7b7ea0328176a8a9eabd9f36be`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Fri, 10 Mar 2023 06:37:36 GMT
RUN Install update 10.0.20348.1607
# Thu, 16 Mar 2023 00:38:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Mar 2023 01:16:54 GMT
ENV JAVA_VERSION=jdk-19.0.2+7
# Thu, 16 Mar 2023 01:25:15 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jre_x64_windows_hotspot_19.0.2_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jre_x64_windows_hotspot_19.0.2_7.msi ;     Write-Host ('Verifying sha256 (4ad4aae081243e6962eddd59c4fdfa33d1a3d79acb16d2700a40dc5d8e4861be) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '4ad4aae081243e6962eddd59c4fdfa33d1a3d79acb16d2700a40dc5d8e4861be') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-19' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 16 Mar 2023 01:25:42 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c921d7eac594f5e3ce3ef10adb8fd0f71bdbb713c4854336b995d25f89c44d42`  
		Last Modified: Thu, 16 Mar 2023 01:41:04 GMT  
		Size: 327.9 MB (327911088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bca4593035ae0e8d1b6e6eb1b053fddc6a6824b28f45f99de726d752d2c0f72`  
		Last Modified: Thu, 16 Mar 2023 01:39:50 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e880df44bcce9ac24c1802639bf4b36af2e701350626da466fa43cf0c60190`  
		Last Modified: Thu, 16 Mar 2023 01:50:41 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c5a17b0904ab0c8cf7d2c56e24363f076ed1dcd7ceafde643434b8567a19386`  
		Last Modified: Thu, 16 Mar 2023 01:52:59 GMT  
		Size: 77.9 MB (77864846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bff92a3fdf4d2160cd7409e4d9a25eaf3678427f3d2ca35f7789fbe2ab63c8`  
		Last Modified: Thu, 16 Mar 2023 01:52:47 GMT  
		Size: 552.6 KB (552638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:19-jre-windowsservercore` - windows version 10.0.17763.4131; amd64

```console
$ docker pull eclipse-temurin@sha256:b0cd3c41a7e94918cc93289d1ba6631a04a5a6da09f1946a6753690a06d18298
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2094467643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83704367b058463c55314d5634b8d9c5a578be26ff8f24ce38f1299b1c0cb968`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Sat, 11 Mar 2023 10:37:22 GMT
RUN Install update 10.0.17763.4131
# Thu, 16 Mar 2023 00:41:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Mar 2023 01:19:09 GMT
ENV JAVA_VERSION=jdk-19.0.2+7
# Thu, 16 Mar 2023 01:27:26 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jre_x64_windows_hotspot_19.0.2_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jre_x64_windows_hotspot_19.0.2_7.msi ;     Write-Host ('Verifying sha256 (4ad4aae081243e6962eddd59c4fdfa33d1a3d79acb16d2700a40dc5d8e4861be) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '4ad4aae081243e6962eddd59c4fdfa33d1a3d79acb16d2700a40dc5d8e4861be') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-19' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 16 Mar 2023 01:28:39 GMT
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
	-	`sha256:25110a113aad9bb60dd17ef9518b688794c3e7e43bdbea5e2afbd4f50b40e7c4`  
		Last Modified: Thu, 16 Mar 2023 01:51:26 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44dd8968c9070563f1f44d0922374f39ded7847801fdc76a70fef89621dfcfc9`  
		Last Modified: Thu, 16 Mar 2023 01:53:20 GMT  
		Size: 77.6 MB (77637350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdcffbe7d7e9492ce8ca26aa02429dfd30de9972e4d209f8eb0543f8ad8c636`  
		Last Modified: Thu, 16 Mar 2023 01:53:09 GMT  
		Size: 3.3 MB (3318501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
