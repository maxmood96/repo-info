## `eclipse-temurin:21-jre-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:bb8e358faccc96af80eaffe97237bade6a486be713f8adc09ca7d7046651538d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:21-jre-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull eclipse-temurin@sha256:6d590e17dd2b712a604471872cc88e2fb7ef9e33e1353c5e7515c1e7cbbc236a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2210132556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:622d8badced2f1e8c4e3c426128d3989150d0e9dc5fb1b69d200bd228f9ba1e0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Tue, 14 Jan 2025 23:34:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:34:55 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Tue, 14 Jan 2025 23:35:53 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_x64_windows_hotspot_21.0.5_11.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_x64_windows_hotspot_21.0.5_11.msi ;     Write-Host ('Verifying sha256 (baa356843cbe2cbc8e49bad1cfef27eaaf5e59748a1627be40492804753c706a) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'baa356843cbe2cbc8e49bad1cfef27eaaf5e59748a1627be40492804753c706a') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 14 Jan 2025 23:36:01 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4a920c12dc6e0111173974f2433565cf5ad3596b6babf34e488eb4da543445`  
		Last Modified: Tue, 14 Jan 2025 23:36:03 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e7c1c8e554ab148504a2c484e60e5e264c5d4caae789f3bcda2cdf09a1262bf`  
		Last Modified: Tue, 14 Jan 2025 23:36:03 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6bf1c13af4b6d524710591b44a8c7add8869facb163ad231457b21aa536072`  
		Last Modified: Tue, 14 Jan 2025 23:36:10 GMT  
		Size: 84.3 MB (84310874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989a89daded90ca51b82f956526fe9f9267e662ddda4a8b07a2c5183f4beda08`  
		Last Modified: Tue, 14 Jan 2025 23:36:04 GMT  
		Size: 3.6 MB (3606879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
