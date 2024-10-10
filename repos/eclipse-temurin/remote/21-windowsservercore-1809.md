## `eclipse-temurin:21-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:d3cae4568853d7e263be37155616c1127225516ca52ec5fb2ed0735a71e84fca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `eclipse-temurin:21-windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull eclipse-temurin@sha256:d9ff0b4c414e676c38f95003e828a3e4ae53b2dc016680ac660b7401e36343bb
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2284872315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc07cc751070ea22f127d805578ec11c596260ac807eb7d56768432bcc48af82`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Wed, 09 Oct 2024 23:35:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 23:58:13 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Wed, 09 Oct 2024 23:59:34 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_windows_hotspot_21.0.4_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_windows_hotspot_21.0.4_7.msi ;     Write-Host ('Verifying sha256 (5eadbdeabdca1a7abf6416a6b35bf7afd86e7edade7b5d44059fbcecacaef372) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '5eadbdeabdca1a7abf6416a6b35bf7afd86e7edade7b5d44059fbcecacaef372') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 10 Oct 2024 00:00:11 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 10 Oct 2024 00:00:11 GMT
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
	-	`sha256:71416d65806874920ade48cad9fe9e847b67ca207c59353ff136f87da9c117ce`  
		Last Modified: Thu, 10 Oct 2024 00:19:58 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc751f056192cff9f7bfd4fbf85ed9b28a75d2f9d7f9d5361e9729cc14189be4`  
		Last Modified: Thu, 10 Oct 2024 00:28:30 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d1f0edc16ba0433e9b9b48904a3d18019925f90ae8277032f04117818a6f82`  
		Last Modified: Thu, 10 Oct 2024 00:28:56 GMT  
		Size: 379.0 MB (379040868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d926a71c44908ce51fbb9fefd18b37da7f64cb6e8085aa69dfa60440ae49117e`  
		Last Modified: Thu, 10 Oct 2024 00:28:31 GMT  
		Size: 4.0 MB (4001932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ffba8f3bb40dc1b4545bde5496c2b12c482114e20e02077b64dcf0568889d8`  
		Last Modified: Thu, 10 Oct 2024 00:28:30 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
