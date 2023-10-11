## `eclipse-temurin:21_35-jdk-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:e480daa848e02f1f0c5271cf547e6eb8c8bc761fbfecf7cf0c2fc5e6fff1cdd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `eclipse-temurin:21_35-jdk-windowsservercore-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull eclipse-temurin@sha256:0db288aaae0906f0e17a69219c12619d3242d825ac9c07968cca77a12365c904
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2414280921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c33049fd969f18ba05951fde77f82ced43597f2ae17224906b7a82d9c682197`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 01:36:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 17:34:42 GMT
ENV JAVA_VERSION=jdk-21+35
# Wed, 11 Oct 2023 17:36:24 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21%2B35/OpenJDK21U-jdk_x64_windows_hotspot_21_35.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21%2B35/OpenJDK21U-jdk_x64_windows_hotspot_21_35.msi ;     Write-Host ('Verifying sha256 (420b09998ae215154b6665c4d8167a74fd99eb3d4d85d5657ba317666e65e301) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '420b09998ae215154b6665c4d8167a74fd99eb3d4d85d5657ba317666e65e301') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 11 Oct 2023 17:37:30 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 11 Oct 2023 17:37:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0814e4a0bb8c615854a85a2b60cd043cfd20ad5a5d755acab1b30b18e4bfad3c`  
		Last Modified: Wed, 11 Oct 2023 02:46:41 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b26c12848d469db2241a06d186840577de0744b88357c91115183b9974ddeaf3`  
		Last Modified: Wed, 11 Oct 2023 17:47:32 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7e92bd98b14973c80db620925562df11985537434fedf8e8111f8de0f76884`  
		Last Modified: Wed, 11 Oct 2023 17:48:04 GMT  
		Size: 378.7 MB (378670945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13bbb179a3f4befba7b67dbdcd934fe5496f3a051d30587755d4d788c2491fdc`  
		Last Modified: Wed, 11 Oct 2023 17:47:33 GMT  
		Size: 4.0 MB (4015335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4aec5ef14f3734cc546f309fff94d1e3f98f4918a8efc02c851a745a8d08e0`  
		Last Modified: Wed, 11 Oct 2023 17:47:32 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
