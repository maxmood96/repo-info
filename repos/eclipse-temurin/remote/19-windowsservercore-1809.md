## `eclipse-temurin:19-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:fa2a3c3dfc8fc8ac9d84334317d48035690ed65029bc1c2c0435f2b478caf94a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3887; amd64

### `eclipse-temurin:19-windowsservercore-1809` - windows version 10.0.17763.3887; amd64

```console
$ docker pull eclipse-temurin@sha256:3bcec20f0207c2659adb029d1365fd213d43cf98fd474b085f7e056b59f75cb0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2078593371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f209f0d1b43595b14e8486300b92087e438411b02d5a7c559aa8ef9595c6cc38`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 02:12:18 GMT
ENV JAVA_VERSION=jdk-19.0.1+10
# Thu, 12 Jan 2023 02:13:32 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jdk_x64_windows_hotspot_19.0.1_10.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jdk_x64_windows_hotspot_19.0.1_10.msi ;     Write-Host ('Verifying sha256 (d4e742c37e645f4b1fa40734df75949ae0ecd5cd946f8dac241d58924a63e787) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'd4e742c37e645f4b1fa40734df75949ae0ecd5cd946f8dac241d58924a63e787') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-19' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 12 Jan 2023 02:14:03 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 12 Jan 2023 02:14:04 GMT
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
	-	`sha256:f43538d48c766ce9df016fea6195b32a6a3e770edf0c7d8409c5744f76b02853`  
		Last Modified: Thu, 12 Jan 2023 02:48:22 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:902552d9809a48c44cecb4fc931377e9b96dd69a77658cf10687ab39cced82bd`  
		Last Modified: Thu, 12 Jan 2023 02:48:56 GMT  
		Size: 366.7 MB (366689228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561603250ee98bf066eda1aae4c7fd3beb1cb60a2d40bb90cad93210da419c16`  
		Last Modified: Thu, 12 Jan 2023 02:48:24 GMT  
		Size: 4.0 MB (3955943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8de6a6305b5b96e4cf206892d2dcb47da21ba5bc54ff90044b2732acce5b8ba`  
		Last Modified: Thu, 12 Jan 2023 02:48:22 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
