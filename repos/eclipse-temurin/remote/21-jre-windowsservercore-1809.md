## `eclipse-temurin:21-jre-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:57d7f90473100875d206a024aa5ef6daf56e32a1af7dd5507146c3472f77f335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `eclipse-temurin:21-jre-windowsservercore-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull eclipse-temurin@sha256:aa40d98b7a04a2cc7bbece45b2685cd8bf17e41d641b0230f326fe446ec2a2f7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2098772965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a33b37463a97af3bbfb304c397d06f9173c391052c423f79259d3a5151ed90`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Thu, 14 Nov 2024 20:10:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 20:10:55 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Thu, 14 Nov 2024 20:11:28 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_x64_windows_hotspot_21.0.5_11.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_x64_windows_hotspot_21.0.5_11.msi ;     Write-Host ('Verifying sha256 (baa356843cbe2cbc8e49bad1cfef27eaaf5e59748a1627be40492804753c706a) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'baa356843cbe2cbc8e49bad1cfef27eaaf5e59748a1627be40492804753c706a') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 14 Nov 2024 20:11:37 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed9a867a4ec0a97835ffbd244b2fb4db0985c0bdd19f13ef9a2f306d5ad4fc82`  
		Last Modified: Thu, 14 Nov 2024 20:11:41 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc9a61adb6ebc54a19a4f524445a15014cd7ac7fba41baf1a37f6d13615723b`  
		Last Modified: Thu, 14 Nov 2024 20:11:41 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6054edab3962e0d388762e242350f7924b82c7fc756f4edef32fb2f19e23e7`  
		Last Modified: Thu, 14 Nov 2024 20:11:49 GMT  
		Size: 84.5 MB (84477045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf04af61ed9e6f2f7d7ad7ece3e6e7705c9d46e1c3c0513a6f08b34ff436c3f`  
		Last Modified: Thu, 14 Nov 2024 20:11:42 GMT  
		Size: 3.6 MB (3639426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
