## `eclipse-temurin:17-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:17a6766aedd1db49436a99e20c6ff4add272d3c06206bf20a173ab2d2242b9ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1487; amd64
	-	windows version 10.0.17763.3887; amd64

### `eclipse-temurin:17-windowsservercore` - windows version 10.0.20348.1487; amd64

```console
$ docker pull eclipse-temurin@sha256:b625d7b196bccb86a193adbe68b9b4960919ab4b38afa038a1ec5619184d03e8
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1739308947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1cdb5b708c6aff3dc4b7d555fcd49a652a1aca665a8e77f4a452276b4bafd1`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Thu, 12 Jan 2023 01:40:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 02:01:43 GMT
ENV JAVA_VERSION=jdk-17.0.5+8
# Thu, 12 Jan 2023 02:02:58 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jdk_x64_windows_hotspot_17.0.5_8.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jdk_x64_windows_hotspot_17.0.5_8.msi ;     Write-Host ('Verifying sha256 (33a2d3d25d83cc6c7e5e7267bfa4c262319555f402d771ce1e05abbf52183391) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '33a2d3d25d83cc6c7e5e7267bfa4c262319555f402d771ce1e05abbf52183391') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 12 Jan 2023 02:03:27 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 12 Jan 2023 02:03:28 GMT
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
	-	`sha256:917264bff9dd61f41fb674eae46aa8b4e03e09c30ac0e7d1c1ab69133d600c38`  
		Last Modified: Thu, 12 Jan 2023 02:44:42 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef23e9d059cf975bc470caf6758d7425c48b15af97d7102bdde5ee18a95fd045`  
		Last Modified: Thu, 12 Jan 2023 02:45:18 GMT  
		Size: 352.7 MB (352709191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b4d7ed7519311837b6112fdecc9b12579ca94237ff292531bafa086f0f72aa`  
		Last Modified: Thu, 12 Jan 2023 02:44:43 GMT  
		Size: 566.4 KB (566381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:968dc753b9838263f5c3c3256f04bafa4b12a78c170e2dd7df19867d16b05a4f`  
		Last Modified: Thu, 12 Jan 2023 02:44:42 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-windowsservercore` - windows version 10.0.17763.3887; amd64

```console
$ docker pull eclipse-temurin@sha256:27dfe8b422fd8161b4b95aec027a17a6d6b757a88e475243a25520bf4f678f23
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2064335148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e59bef352d3eef1ffaffaa99a151a78d09dc267cbbebef02b195ed10bab55d70`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 02:03:47 GMT
ENV JAVA_VERSION=jdk-17.0.5+8
# Thu, 12 Jan 2023 02:04:59 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jdk_x64_windows_hotspot_17.0.5_8.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jdk_x64_windows_hotspot_17.0.5_8.msi ;     Write-Host ('Verifying sha256 (33a2d3d25d83cc6c7e5e7267bfa4c262319555f402d771ce1e05abbf52183391) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '33a2d3d25d83cc6c7e5e7267bfa4c262319555f402d771ce1e05abbf52183391') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 12 Jan 2023 02:05:35 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 12 Jan 2023 02:05:36 GMT
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
	-	`sha256:5cc1e02ea42ee65c5b959bfd1e568eabfcb5918a4bb62c3ad6ba2e3431e07e42`  
		Last Modified: Thu, 12 Jan 2023 02:45:29 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672f12eb163ed11752821aa965dd5579e4b07e3b96ed98583779edf4fe4dffd3`  
		Last Modified: Thu, 12 Jan 2023 02:46:01 GMT  
		Size: 352.5 MB (352486595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6defb85ea5e9c5a3ac8bed105802762c92ddf6c835024caeef86608a59d86c99`  
		Last Modified: Thu, 12 Jan 2023 02:45:31 GMT  
		Size: 3.9 MB (3900465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cae44834d0d00112a35ac616bff17624fa799c3cda43f37813fe7a3b90f5eb5`  
		Last Modified: Thu, 12 Jan 2023 02:45:28 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
