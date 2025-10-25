## `eclipse-temurin:11-jdk-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:310c2815eea972413e5d291b08bd2eab779040ec607865c14bb8008e5a07edf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `eclipse-temurin:11-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.6905; amd64

```console
$ docker pull eclipse-temurin@sha256:1e4823da5588c6f1a5c1e0c83b4d62db4c397ebd69917242335b2739202d3078
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3589992645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c08bb11da56ec60be069b92fc1389a09efbf122cb525dd846c18086c1b75b4c1`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 24 Oct 2025 18:13:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:13:33 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Fri, 24 Oct 2025 18:14:11 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_x64_windows_hotspot_11.0.28_6.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_x64_windows_hotspot_11.0.28_6.msi ;     Write-Host ('Verifying sha256 (5063082c0f8a35e2d033ae1ca64eea7ab02222cf04ec97b8318426443f9e1cb0) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '5063082c0f8a35e2d033ae1ca64eea7ab02222cf04ec97b8318426443f9e1cb0') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 24 Oct 2025 18:14:17 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:14:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571af3b90b3defe521c8285732a5f27a7d3abdaa40750b1b3e6b3d6208a2b69d`  
		Last Modified: Fri, 24 Oct 2025 18:23:19 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb6cd957181925f949886019ab615c9e10d32d5de6958883a11bdca388bb852`  
		Last Modified: Fri, 24 Oct 2025 18:23:16 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edcb2d302a56dad1e1b04ed4092069dd59fb749970b91acfeddc3f0a18d14e53`  
		Last Modified: Fri, 24 Oct 2025 19:18:23 GMT  
		Size: 369.3 MB (369300709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3eb78f57e1084b702347eadedb190236bceaa196482592570ab1fe0dae8e777`  
		Last Modified: Fri, 24 Oct 2025 18:23:17 GMT  
		Size: 341.0 KB (341037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f7c7634ab4e23c0d3d6adaff9b8c22660a36b622b05a1520b06aac62f8a639`  
		Last Modified: Fri, 24 Oct 2025 18:23:16 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
