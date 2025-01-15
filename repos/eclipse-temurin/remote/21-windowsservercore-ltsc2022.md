## `eclipse-temurin:21-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:6efdb2a7b0a86c69a21df7a602f5472680f39679ab2d7eec379c201690ea4b47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `eclipse-temurin:21-windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull eclipse-temurin@sha256:1a1c83881be5949a0569914395e0eeb4d96eb0964d85e3c09f27470260506406
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2644555794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1702e2ecace9ef44851d7f84927d8d8612fb5b95b8b198eecb8e02e9621507e7`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Tue, 14 Jan 2025 23:37:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:37:18 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Tue, 14 Jan 2025 23:37:51 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_x64_windows_hotspot_21.0.5_11.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_x64_windows_hotspot_21.0.5_11.msi ;     Write-Host ('Verifying sha256 (8ef78a37811529d73d37e29a9fa24bf2d46d0d5d97c4f6e403ea9adebc55eaf3) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '8ef78a37811529d73d37e29a9fa24bf2d46d0d5d97c4f6e403ea9adebc55eaf3') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 14 Jan 2025 23:37:59 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:38:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dab86350c4bd3fec13909a27b3d2720d0c5ca9ec68e5fc4b82cb72ba58abf74`  
		Last Modified: Tue, 14 Jan 2025 23:38:03 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883719ffea6c90b780f01abf0aa4c161368dbb3725f461b0fdd779ee19e1455c`  
		Last Modified: Tue, 14 Jan 2025 23:38:03 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177a63e3228dbbc48022a0c51d9e42bc9d700a7944af28638103bef76318c6cb`  
		Last Modified: Tue, 14 Jan 2025 23:38:18 GMT  
		Size: 381.8 MB (381812291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae766186a789c38a4d8ef85325e8d2424ee95ec2648f5a8851f8d1563d7a861`  
		Last Modified: Tue, 14 Jan 2025 23:38:03 GMT  
		Size: 354.4 KB (354398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a5996503133197b15f5acbd789651248aafc2f91fa14c8c50a565572028dc2`  
		Last Modified: Tue, 14 Jan 2025 23:38:03 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
