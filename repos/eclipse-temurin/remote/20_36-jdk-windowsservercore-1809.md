## `eclipse-temurin:20_36-jdk-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:4d28c070c99d6005ace387b8ec143b87841bb4bd44552251b13c6a242b849a9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4131; amd64

### `eclipse-temurin:20_36-jdk-windowsservercore-1809` - windows version 10.0.17763.4131; amd64

```console
$ docker pull eclipse-temurin@sha256:f9536602e459435d7c590f9fccef6c84dc9a4e7e2d237ad6f6f47ba755acdc0b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2387222017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8393f45c998b59278d9a696390b094dde0d0c34f7485f830016e6672a311ae6`
-	Default Command: `["jshell"]`
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
# Mon, 27 Mar 2023 20:23:34 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20%2B36/OpenJDK20U-jdk_x64_windows_hotspot_20_36.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20%2B36/OpenJDK20U-jdk_x64_windows_hotspot_20_36.msi ;     Write-Host ('Verifying sha256 (d4e41a6fce8f86dabb0422231f4723579021479eb9331cd9d07fb01c4126a022) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'd4e41a6fce8f86dabb0422231f4723579021479eb9331cd9d07fb01c4126a022') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-20' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Mon, 27 Mar 2023 20:25:09 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Mon, 27 Mar 2023 20:25:11 GMT
CMD ["jshell"]
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
	-	`sha256:5e0a016d1b3135a635bdf4b91005825b8e044007fa1e298c069324376bf99ac0`  
		Last Modified: Mon, 27 Mar 2023 20:38:16 GMT  
		Size: 369.7 MB (369677795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050e4872a112735056825c815db2920ab36b68dd852bb5849fcb27d91b4c9160`  
		Last Modified: Mon, 27 Mar 2023 20:37:45 GMT  
		Size: 4.0 MB (4030954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb1ce86a435cf2f25d4c4ddd4c299784c4a2755eef771b52e926912dbc562b5`  
		Last Modified: Mon, 27 Mar 2023 20:37:44 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
