## `eclipse-temurin:21-jre-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:9320743dad9280e2a2276178077f1a250c8a5f66adfd2713dde6dd7298a0c3a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `eclipse-temurin:21-jre-windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull eclipse-temurin@sha256:51fa21400e0993aa3a22a58cf9caf49b284add917aeb9a67294f07e9d8bbd2e4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2266737959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:535e6d58663070e31ac211bae50a5f96f4c25d09785679b047473d323824f0ec`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 19:38:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 20:12:17 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Wed, 15 May 2024 20:19:29 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_x64_windows_hotspot_21.0.3_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_x64_windows_hotspot_21.0.3_9.msi ;     Write-Host ('Verifying sha256 (790bd6bd823618ce33e366294159282b92d3fcd41886e375fd4b876843e0d90f) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '790bd6bd823618ce33e366294159282b92d3fcd41886e375fd4b876843e0d90f') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 15 May 2024 20:20:49 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716a2aa6d68dd7a7e7745c65cd54a1e2713d737d3f4fdd07e5e1c2fce38b5d24`  
		Last Modified: Wed, 15 May 2024 20:44:17 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5127ab5a85ec0f5417347add1b1557d2c76b9868ce8480a88cf9ae5375bf8f8`  
		Last Modified: Wed, 15 May 2024 20:53:09 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff75a8dcb35ee71d4392abbb7b3724053d291db37cc727293886d9607aaf769`  
		Last Modified: Wed, 15 May 2024 20:54:49 GMT  
		Size: 83.5 MB (83482780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b03de62dba7c58e105f243d3482d809e9e82c8e68ee05a07c9aeb2cec48fd9`  
		Last Modified: Wed, 15 May 2024 20:54:39 GMT  
		Size: 3.5 MB (3541035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
