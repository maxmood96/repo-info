## `eclipse-temurin:11-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:a655f5f86c8ce8c7a215c794119f9130366b6c72e02929cedbc136a0c297715b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `eclipse-temurin:11-windowsservercore` - windows version 10.0.20348.2762; amd64

```console
$ docker pull eclipse-temurin@sha256:b1a35b0291162f779107c4da34e992674cba3cea2adbf161151f1e1757492328
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2167347800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46cacc53876ea173b7d7b83d42c09d83b97afc890d49a801bc2b0daa4888ced9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Sat, 19 Oct 2024 00:54:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 19 Oct 2024 00:54:54 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Sat, 19 Oct 2024 00:56:18 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_x64_windows_hotspot_11.0.24_8.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_x64_windows_hotspot_11.0.24_8.msi ;     Write-Host ('Verifying sha256 (c6d15bff637a78d2033cd42c592e47c09fe87e7d028ae7d1fbf591c547848917) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'c6d15bff637a78d2033cd42c592e47c09fe87e7d028ae7d1fbf591c547848917') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Sat, 19 Oct 2024 00:56:25 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Sat, 19 Oct 2024 00:56:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66c5aafd71231e60b79ceeb2d14d2f93445b7dc03610de950e5b4d36d18c8430`  
		Last Modified: Sat, 19 Oct 2024 00:56:28 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c622161dee949b75630081e617917799c39fb9a67ae2eb54d23e4f7372d76b9`  
		Last Modified: Sat, 19 Oct 2024 00:56:28 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b4eacd08cd961187d90ae8dcd26985ee7a76cf70f235f5f95e3139d7f95872`  
		Last Modified: Sat, 19 Oct 2024 00:56:42 GMT  
		Size: 367.7 MB (367688541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:375d393676580ea3d143d50adad7f4bfdd834ac5282157c2f5cff36de7c3f700`  
		Last Modified: Sat, 19 Oct 2024 00:56:29 GMT  
		Size: 313.8 KB (313849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc120e1809b474ab79a22cd24fa1a7612ff16de8d7ba6d8b44fba9bf514873e`  
		Last Modified: Sat, 19 Oct 2024 00:56:28 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull eclipse-temurin@sha256:6ba040573380c9a1d0a647c6f7e1a8b9272744ccd9cb950f96d9b4fc2c5309d4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2269849274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c8facfe818c3fafd73951174ae06c3b6239bb26ab56a50f933930c69a2a9a85`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Sat, 19 Oct 2024 00:55:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 19 Oct 2024 00:55:14 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Sat, 19 Oct 2024 00:57:57 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_x64_windows_hotspot_11.0.24_8.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_x64_windows_hotspot_11.0.24_8.msi ;     Write-Host ('Verifying sha256 (c6d15bff637a78d2033cd42c592e47c09fe87e7d028ae7d1fbf591c547848917) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'c6d15bff637a78d2033cd42c592e47c09fe87e7d028ae7d1fbf591c547848917') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Sat, 19 Oct 2024 00:58:07 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Sat, 19 Oct 2024 00:58:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f2e8da257bcfd2296d4cb27c98e42a62c588aec191344bbf2e669d660dc5118`  
		Last Modified: Sat, 19 Oct 2024 00:58:10 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb3f521b7eebb0937f9f3537b3a574857d71dc5f1e39ff26ff617f45c79db77`  
		Last Modified: Sat, 19 Oct 2024 00:58:10 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0284ab50d026404528a930b947ff7d6048691ce27aa6fbebd390a556ee747f5b`  
		Last Modified: Sat, 19 Oct 2024 00:58:24 GMT  
		Size: 367.7 MB (367710453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c35fbe24a9d82a085c75d5b522718a4409111c5d7e6420a684e2d12b84f1cc60`  
		Last Modified: Sat, 19 Oct 2024 00:58:11 GMT  
		Size: 309.7 KB (309672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf18fcedef574c3b97e62351497cb03c7e38f77451e9ea5ce48fae5d52879a3`  
		Last Modified: Sat, 19 Oct 2024 00:58:10 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
