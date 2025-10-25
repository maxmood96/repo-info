## `eclipse-temurin:11-jre-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:78f360a50816424d405af8b498c415a742e53afeabc44d122f864ffc875e04cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `eclipse-temurin:11-jre-windowsservercore-ltsc2025` - windows version 10.0.26100.6905; amd64

```console
$ docker pull eclipse-temurin@sha256:85872aa8e2cb0489f15afdcc93a200c9c342153fb2930ed7b0d8d72604984f9d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3295615734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ed6bdcdcb81b2347bbf34b9f3368e24b033e112bda8cf1fbcca0650e5c31a23`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 24 Oct 2025 18:13:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:13:22 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Fri, 24 Oct 2025 18:13:43 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_x64_windows_hotspot_11.0.28_6.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_x64_windows_hotspot_11.0.28_6.msi ;     Write-Host ('Verifying sha256 (a093e7c3b7754bcf61140764eddb11343e3810890dcc3b96195b7d695cd1358b) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'a093e7c3b7754bcf61140764eddb11343e3810890dcc3b96195b7d695cd1358b') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 24 Oct 2025 18:13:49 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
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
	-	`sha256:2306afc06fe394817b697769f818a638f384b35e7a7bdcfd10e74c6c7ee210f8`  
		Last Modified: Fri, 24 Oct 2025 18:23:16 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c27ac2cb190f8e2c9057e89ae7924df16b3a21fe69976bc7a0440819bedd3202`  
		Last Modified: Fri, 24 Oct 2025 18:23:16 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbe775f4998dba702429cd80aa208c1ad86e0d08397a24afb570e65fd88033a`  
		Last Modified: Fri, 24 Oct 2025 18:23:22 GMT  
		Size: 74.9 MB (74911481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c859d7d57d041776ec2803b5f63cc7e34973a3d49826f09663f63590023ab2a`  
		Last Modified: Fri, 24 Oct 2025 18:23:16 GMT  
		Size: 354.6 KB (354638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
