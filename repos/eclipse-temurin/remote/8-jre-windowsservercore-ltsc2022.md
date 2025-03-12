## `eclipse-temurin:8-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:9b1618c7c3a1111f249367243cbc82386e41822996e86c7ac1322aceffffaeb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `eclipse-temurin:8-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull eclipse-temurin@sha256:78e84c8e3f264de85bc87b7acc20abc24f41e0335ee7a911e7e843dff5d2967f
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2343047664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b27af9c4954a763964e2f0834a7314e5c0603c656d0e693ecfc97a40f01b76ad`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Wed, 12 Mar 2025 18:53:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:53:32 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Wed, 12 Mar 2025 18:53:52 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_x64_windows_hotspot_8u442b06.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_x64_windows_hotspot_8u442b06.msi ;     Write-Host ('Verifying sha256 (4dd03622b9690427dbcd6df6c60eb6e1a422f1eb7389f0d08ef844bf43e23eab) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '4dd03622b9690427dbcd6df6c60eb6e1a422f1eb7389f0d08ef844bf43e23eab') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Mar 2025 18:53:59 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e747f4c10c6562caea6af08509b2c5abe2cd6e5545a4f0f1503b92700b50a862`  
		Last Modified: Wed, 12 Mar 2025 18:54:01 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:331827ca3a7edf91f9a1757127d8c59f548d85a42a55998037fa72d1b051d27e`  
		Last Modified: Wed, 12 Mar 2025 18:54:01 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3bc894ef87cef9dc563acdefedae76d3fe8dcce352698e6be7e1b63c7e89a1`  
		Last Modified: Wed, 12 Mar 2025 18:54:06 GMT  
		Size: 72.8 MB (72750311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e778bd926aed5c140d1ad7282863bb391e30e580f1e0ed811d1ce19bd181d36b`  
		Last Modified: Wed, 12 Mar 2025 18:54:01 GMT  
		Size: 353.6 KB (353571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
