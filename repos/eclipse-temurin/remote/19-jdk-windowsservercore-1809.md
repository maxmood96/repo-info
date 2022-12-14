## `eclipse-temurin:19-jdk-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:728e28b0285b86339ea5009d7e07a363362a20fbbea5fe58dc26f63873365507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3770; amd64

### `eclipse-temurin:19-jdk-windowsservercore-1809` - windows version 10.0.17763.3770; amd64

```console
$ docker pull eclipse-temurin@sha256:ce78a55b989edcc1ceef7b8be6997a06c336c33a5355a20395abdbb36cc49d8c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 GB (3151314586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850a2b7f9f102a37cc401d9debe9a326bacf41e9eb67e5e76b0e461dce4a6e81`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sun, 11 Dec 2022 08:04:49 GMT
RUN Install update 10.0.17763.3770
# Tue, 13 Dec 2022 22:48:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Dec 2022 23:31:20 GMT
ENV JAVA_VERSION=jdk-19.0.1+10
# Tue, 13 Dec 2022 23:33:34 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jdk_x64_windows_hotspot_19.0.1_10.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jdk_x64_windows_hotspot_19.0.1_10.msi ;     Write-Host ('Verifying sha256 (d4e742c37e645f4b1fa40734df75949ae0ecd5cd946f8dac241d58924a63e787) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'd4e742c37e645f4b1fa40734df75949ae0ecd5cd946f8dac241d58924a63e787') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-19' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 13 Dec 2022 23:35:15 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 13 Dec 2022 23:35:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3ad73ed772f80ab7923579a55dd12fb9b6e090d1d836408d16ffd9d3dee252`  
		Last Modified: Tue, 13 Dec 2022 23:56:47 GMT  
		Size: 856.4 MB (856427878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc9debb9503ac53c2f64685982eca56ac5110ea6baf7278b27af54ab8fbc409`  
		Last Modified: Tue, 13 Dec 2022 23:54:25 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d102d204a272596ec386dd5585ee6e2ed63f8ed6a968ceae8cf0dd31e4d74833`  
		Last Modified: Wed, 14 Dec 2022 00:05:18 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:487ef9525b3b8178d2ce6005a12a85afe52c61c0bddb2dd991a628ebffe207c9`  
		Last Modified: Wed, 14 Dec 2022 00:05:52 GMT  
		Size: 366.7 MB (366669040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf104ddea85424c35622443fe835ccf4e50dce34dd26ebd41a89a804d7baaa43`  
		Last Modified: Wed, 14 Dec 2022 00:05:20 GMT  
		Size: 3.9 MB (3944080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb226464293c8f38271ba715776d85f13864f32d85b531b4e984d2aa0f21e22c`  
		Last Modified: Wed, 14 Dec 2022 00:05:18 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
