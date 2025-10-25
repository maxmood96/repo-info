## `eclipse-temurin:11-jdk-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:904a5850319a19db6129ce3e470ef04bf833001bc60b516203437f80f2ed51e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `eclipse-temurin:11-jdk-windowsservercore` - windows version 10.0.26100.6905; amd64

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

### `eclipse-temurin:11-jdk-windowsservercore` - windows version 10.0.20348.4297; amd64

```console
$ docker pull eclipse-temurin@sha256:34c08e54cf7d3e24efd8482cdd3108c6aeec4b0982c9f66eb5aadbf41f25d211
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1946996384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0c50a4d8caf0585fa3e8e1a67dec7987e3159ec80a69de8f71e4b9925e0637`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:10:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:21:04 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Fri, 24 Oct 2025 18:21:39 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_x64_windows_hotspot_11.0.28_6.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_x64_windows_hotspot_11.0.28_6.msi ;     Write-Host ('Verifying sha256 (5063082c0f8a35e2d033ae1ca64eea7ab02222cf04ec97b8318426443f9e1cb0) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '5063082c0f8a35e2d033ae1ca64eea7ab02222cf04ec97b8318426443f9e1cb0') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 24 Oct 2025 18:21:48 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:21:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:116a61045287ead6d3e96e549433b65e0cd74ce2180f5ec4df258d66b09b85a4`  
		Last Modified: Fri, 24 Oct 2025 18:20:52 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8d1bc9100ec65450255fe3fafd36ffc7d5d58c75b0e8b513bb25d1d88fb2ad`  
		Last Modified: Fri, 24 Oct 2025 18:22:19 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df644d9db3373e4e0cfd337ce36a8f7928741eb3f2473de9314eedd6197bad7d`  
		Last Modified: Fri, 24 Oct 2025 19:20:28 GMT  
		Size: 369.4 MB (369449577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23446d71c34f3547baaa613e680b2a9c2263310f2ca34186737529f7d5f7baf0`  
		Last Modified: Fri, 24 Oct 2025 18:22:19 GMT  
		Size: 349.9 KB (349914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7953d3b8c3da69b1bc13476d7b8e97d217b62ef1e48fa3c7e8802112b8b20ac1`  
		Last Modified: Fri, 24 Oct 2025 18:22:20 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
