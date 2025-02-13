## `eclipse-temurin:11-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:74ae05a1990060243da67eece1c5f1d16a8235464a8b1ff97ea82338eff84f46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `eclipse-temurin:11-windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull eclipse-temurin@sha256:762017571016d50a605feb792b4579194a96bc2f3a54679dbbc797dba30996e0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2632051578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:684ef2b9ef164dfbab291b9f931e2606a72ae15ab2060aa699e45dcee71f55a4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Fri, 31 Jan 2025 02:12:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Jan 2025 02:12:13 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Fri, 31 Jan 2025 02:12:52 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_windows_hotspot_11.0.26_4.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_windows_hotspot_11.0.26_4.msi ;     Write-Host ('Verifying sha256 (25bc11bd05e4dad95ebefde017bd5eb29dfe8624bbd46beeca8eba4b4d77fae1) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '25bc11bd05e4dad95ebefde017bd5eb29dfe8624bbd46beeca8eba4b4d77fae1') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 31 Jan 2025 02:13:01 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Fri, 31 Jan 2025 02:13:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 21:54:27 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5eff04532649c1cc24a7a1a077ef832362bd7bad25840a148def2b710d7aa51`  
		Last Modified: Wed, 05 Feb 2025 15:08:34 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b4b08b2f379d50ad034f14cd7e51e436414cb2a6cd7f8df494e69c3734d89e`  
		Last Modified: Wed, 05 Feb 2025 04:44:17 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc026f9cc8bd26d6b37bbc404deb6c7fe811828d768ea99927a4d8497ff59a29`  
		Last Modified: Thu, 06 Feb 2025 06:52:49 GMT  
		Size: 369.3 MB (369302403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7edebfdfab99905a0941cfc03a1e23891ad78a6ec8a390785bac218ba8045e07`  
		Last Modified: Mon, 03 Feb 2025 20:46:52 GMT  
		Size: 360.1 KB (360080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a82ac20a053be9e02c5cacfcaa80d78212b5564875b06680e02ab43850b70568`  
		Last Modified: Tue, 04 Feb 2025 20:45:57 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
