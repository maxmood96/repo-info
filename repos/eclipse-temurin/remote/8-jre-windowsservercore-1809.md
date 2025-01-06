## `eclipse-temurin:8-jre-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:e240ae6222025888f23a84584d666cae582e95f9f3d5e5f551803a7d9873caa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `eclipse-temurin:8-jre-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull eclipse-temurin@sha256:500809e74b0cf53ad1fc5e5a84f3e9d3c7c338d341eed43b2b7747e89e9fb8dc
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2087888208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca717ffced14d15bbc380df4c9413c3c36b3a460ac12e592f07eae70659738ee`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:39:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:39:36 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Wed, 11 Dec 2024 20:41:00 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_x64_windows_hotspot_8u432b06.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_x64_windows_hotspot_8u432b06.msi ;     Write-Host ('Verifying sha256 (34801770278c26045517fc1851396d7bf66c7c32fa6f9965b968d55adbebda4b) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '34801770278c26045517fc1851396d7bf66c7c32fa6f9965b968d55adbebda4b') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 11 Dec 2024 20:41:08 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f5665d48b45b3a2a644b19e9937f697224772e90a5261c45ed78b111c18442`  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686ec006a868c72171ace7b0a1f1dd6daf649715a39b6405d7def5b660a048fa`  
		Last Modified: Wed, 11 Dec 2024 20:41:12 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d922278c7717cfd031ff9dd03c4a9fe36fe1459b9f69064cde695159bf6071`  
		Last Modified: Wed, 11 Dec 2024 20:41:17 GMT  
		Size: 73.4 MB (73422129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b9fcf385fa2038b25f0b3000e613756a8b8bb325841afcb06a6812dc251609`  
		Last Modified: Wed, 11 Dec 2024 20:41:12 GMT  
		Size: 293.3 KB (293296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
