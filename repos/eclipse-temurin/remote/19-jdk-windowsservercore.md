## `eclipse-temurin:19-jdk-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:948bfea63be1b663c534aa97bbe490e3e07f47008144ba4b60b03f06d23932c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1487; amd64
	-	windows version 10.0.17763.3887; amd64

### `eclipse-temurin:19-jdk-windowsservercore` - windows version 10.0.20348.1487; amd64

```console
$ docker pull eclipse-temurin@sha256:bb9606a9b66ed9b9a65e0e81a23b6096cf80c40b273b5c31c4f800ad720231a4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1753510257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50b5cae8029bfebf47781c996c1016b012fa17931e55b6ea37bee84dc4b0d538`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Thu, 12 Jan 2023 01:40:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 02:10:04 GMT
ENV JAVA_VERSION=jdk-19.0.1+10
# Thu, 12 Jan 2023 02:11:34 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jdk_x64_windows_hotspot_19.0.1_10.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jdk_x64_windows_hotspot_19.0.1_10.msi ;     Write-Host ('Verifying sha256 (d4e742c37e645f4b1fa40734df75949ae0ecd5cd946f8dac241d58924a63e787) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'd4e742c37e645f4b1fa40734df75949ae0ecd5cd946f8dac241d58924a63e787') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-19' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 12 Jan 2023 02:12:01 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 12 Jan 2023 02:12:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa41f3a43cc9e40e953b9cfe1530c27eed49cf79cdae96e9dfc39b04a1b75ecf`  
		Last Modified: Thu, 12 Jan 2023 02:29:45 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bd00bf56dc1385f89a05fb7a6328aa61a9f3cb567631e33af444269ffd1889d`  
		Last Modified: Thu, 12 Jan 2023 02:47:38 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b7fa48bd4811c03178e5955515233c779518af8cc9f9ca2192b5f074d241c4`  
		Last Modified: Thu, 12 Jan 2023 02:48:11 GMT  
		Size: 366.9 MB (366910567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0057e343bbb8a988f984e3c4199f040bdce1a07b8c71cd037e1e4281cb03c815`  
		Last Modified: Thu, 12 Jan 2023 02:47:39 GMT  
		Size: 566.4 KB (566367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0edcd4011f7429f46c5ddbf3683d99747fbf5798219e8c72742f3050a4ead431`  
		Last Modified: Thu, 12 Jan 2023 02:47:38 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:19-jdk-windowsservercore` - windows version 10.0.17763.3887; amd64

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
