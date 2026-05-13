## `eclipse-temurin:26_35-jre-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:83cb693563b90c608da7de7ea937f8b1dd651d9efa640918bea50826db6c2fb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `eclipse-temurin:26_35-jre-windowsservercore-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull eclipse-temurin@sha256:ce88dabd4d18e41ce264023d67f71f527242098fe9351e3b47575dd92924051f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2310306843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5bb0c93e919d25a38612ee55561de1385958198e45b222443e04c5e6246fb4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Tue, 12 May 2026 23:38:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:46:44 GMT
ENV JAVA_VERSION=jdk-26+35
# Tue, 12 May 2026 23:46:59 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_x64_windows_hotspot_26_35.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_x64_windows_hotspot_26_35.msi ;     Write-Host ('Verifying sha256 (891d4a89535cb0d0451428aa9ce6d87908cc147113b38eef896de6a429052507) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '891d4a89535cb0d0451428aa9ce6d87908cc147113b38eef896de6a429052507') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-26' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 12 May 2026 23:47:06 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47864eebe6f559a2fccc13b4a6a9fea777f2da6d8bbb7f3da933a98004ae1737`  
		Last Modified: Tue, 12 May 2026 23:39:59 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aaa6dfa5d2dab7e97100bc1cea81b331d84a6b7770f89808a68e600047b392b`  
		Last Modified: Tue, 12 May 2026 23:47:10 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1fcd9ac72ba3ef9f8e874305a18bb1d12ea91fcf1846e0ef335184bb1dfca0`  
		Last Modified: Tue, 12 May 2026 23:47:21 GMT  
		Size: 104.0 MB (103995361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ae27ac64f17330b672db1e0daa6c0944c0b62f8fd32716c11d2508be6271fb`  
		Last Modified: Tue, 12 May 2026 23:47:10 GMT  
		Size: 367.0 KB (366958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
