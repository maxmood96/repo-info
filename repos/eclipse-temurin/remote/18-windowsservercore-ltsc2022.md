## `eclipse-temurin:18-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:4154b1bca26eea4ebd184dbf9ef2cd21bf8f75ca6e8c2cc47dfae726634aef5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.887; amd64

### `eclipse-temurin:18-windowsservercore-ltsc2022` - windows version 10.0.20348.887; amd64

```console
$ docker pull eclipse-temurin@sha256:63bfb111f5481e0cc1d5d966cd0e3bc4cad39cc654f270a7cf83930a87a22867
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2672611457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb1cb260fef4c6d968fa3ea462b8d4aafe14c775f8878ec8499d70959977f20`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Sat, 06 Aug 2022 02:59:35 GMT
RUN Install update 10.0.20348.887
# Wed, 10 Aug 2022 12:11:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Aug 2022 16:19:35 GMT
ENV JAVA_VERSION=jdk-18.0.2+9
# Wed, 10 Aug 2022 16:20:33 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_x64_windows_hotspot_18.0.2_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_x64_windows_hotspot_18.0.2_9.msi ;     Write-Host ('Verifying sha256 (b3f9fd4f94e9f117387de4ecbfaf0903a93e64c39683236acba583e75d41ba07) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'b3f9fd4f94e9f117387de4ecbfaf0903a93e64c39683236acba583e75d41ba07') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-18' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 10 Aug 2022 16:20:53 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 10 Aug 2022 16:20:54 GMT
CMD ["jshell"]
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
	-	`sha256:cd5699aa63421faf8f06dc5f3c3be843b73daa755c1b64f0f42e9e4a83afa538`  
		Last Modified: Wed, 10 Aug 2022 16:45:45 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d5b92efa27cd0270d120f225a910bdd411fc7642e31ccea8125e5a1f1a565b`  
		Last Modified: Wed, 10 Aug 2022 16:46:15 GMT  
		Size: 355.1 MB (355148276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f7be7c9c8d4f4232a0d81be888e14c53b598fc2baa58a906c5052d537c1d75`  
		Last Modified: Wed, 10 Aug 2022 16:45:46 GMT  
		Size: 569.8 KB (569772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ce1fb386e7ad948454f179374e0153c26ad3b77c0d9dfa32bd3b9c3f7dd2f5`  
		Last Modified: Wed, 10 Aug 2022 16:45:45 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
