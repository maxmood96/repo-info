## `eclipse-temurin:21-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:4358f1ad1f340bf973717b7a168a0c7357c5dc517d098c6508cc38763bbbba2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `eclipse-temurin:21-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull eclipse-temurin@sha256:7399495ed71be7d400a95e3f94f098da3df085deb1d41f8fc649c356773468f5
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1884116379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a02596d554ee42d48b2d8f30e31d05c6735d9b08fec5908a0a13f1afd5689dba`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Thu, 24 Oct 2024 00:57:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 24 Oct 2024 00:57:50 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Thu, 24 Oct 2024 00:59:19 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_x64_windows_hotspot_21.0.5_11.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_x64_windows_hotspot_21.0.5_11.msi ;     Write-Host ('Verifying sha256 (baa356843cbe2cbc8e49bad1cfef27eaaf5e59748a1627be40492804753c706a) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'baa356843cbe2cbc8e49bad1cfef27eaaf5e59748a1627be40492804753c706a') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 24 Oct 2024 00:59:28 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
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
	-	`sha256:2bd688cef7bd0d9caf8fcb1669aa0d9d79201c5594d319245d57e4469b0c1ac2`  
		Last Modified: Thu, 24 Oct 2024 00:59:30 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d01d3ac75a713582ffc284839bb273907f05bc6ba69a3d711d64001a0db70b1`  
		Last Modified: Thu, 24 Oct 2024 00:59:30 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1283863741b7563b7b959f4290df520df2fb305781c42130b06a7345c30def15`  
		Last Modified: Thu, 24 Oct 2024 00:59:36 GMT  
		Size: 84.4 MB (84444716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0547abe76271269c26eeabf972cbe4a71db1dd49d27835556679487fd081f48a`  
		Last Modified: Thu, 24 Oct 2024 00:59:31 GMT  
		Size: 327.5 KB (327538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
