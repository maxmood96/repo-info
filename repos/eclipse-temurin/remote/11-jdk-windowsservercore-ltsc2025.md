## `eclipse-temurin:11-jdk-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:d8053d3239e623c3de811d395c97858ede3f36a46cda45e30a96f2042011a9c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `eclipse-temurin:11-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull eclipse-temurin@sha256:93726f62a414d069cf6b19125e78e2ec520de573f1178d6ec041cddaa1bc11f1
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 GB (3868536311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abc86ad0eac52ec81ff2d924f11d69d8d2ce19ea1a6749f821074ceaae1aafc0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Tue, 12 Aug 2025 20:26:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:26:58 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Tue, 12 Aug 2025 20:27:17 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_x64_windows_hotspot_11.0.28_6.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_x64_windows_hotspot_11.0.28_6.msi ;     Write-Host ('Verifying sha256 (5063082c0f8a35e2d033ae1ca64eea7ab02222cf04ec97b8318426443f9e1cb0) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '5063082c0f8a35e2d033ae1ca64eea7ab02222cf04ec97b8318426443f9e1cb0') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 12 Aug 2025 20:27:23 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 12 Aug 2025 20:27:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1656ca3b9bb1cf868bd4c2d295b1e59b399e6b45e2bdca4cec91bcea1c8056a6`  
		Last Modified: Tue, 12 Aug 2025 20:31:01 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f314d3eef8bc1475c9e7db0c5cb1625bb2af237a6c96e5c9d59ae52cb810084`  
		Last Modified: Tue, 12 Aug 2025 20:31:01 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dbe16b849a631f645dedee915e945f309983c4529f0ca2c16ef3aaf1d4ff039`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 369.3 MB (369328884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:617e88fe5b76618304479e6cc1ac52be8694ba7cd209ceed1f1fcd2d3f6f1a23`  
		Last Modified: Tue, 12 Aug 2025 20:31:03 GMT  
		Size: 373.0 KB (372991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8369b4b02871826594ba9319d54d7ee80b1d2d2bc482d3fee29457608c4fc570`  
		Last Modified: Tue, 12 Aug 2025 20:31:01 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
