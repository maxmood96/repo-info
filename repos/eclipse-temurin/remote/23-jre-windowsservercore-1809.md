## `eclipse-temurin:23-jre-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:cc3eb36c7c5bc70dadbd16bb16dfc57da9c47461db338e8da0d78a2af5646d88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `eclipse-temurin:23-jre-windowsservercore-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull eclipse-temurin@sha256:08cdbdbc0c38dbdb13f2eeb52182fa3520d20b46cc222546fffb0957ff58a665
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2239288147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a21a96ee9e5c50c959fc98c9e04848bbed44bdf7ea4e2a0071bdd41be1865a8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Wed, 12 Mar 2025 18:53:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:53:08 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Wed, 12 Mar 2025 18:54:16 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_x64_windows_hotspot_23.0.2_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_x64_windows_hotspot_23.0.2_7.msi ;     Write-Host ('Verifying sha256 (07ddf8b8d004692261d0ab769a31176abd22b5203cee44317328f9113a99e486) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '07ddf8b8d004692261d0ab769a31176abd22b5203cee44317328f9113a99e486') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-23' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Mar 2025 18:54:23 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ed62394c2d837cb68372e0f304c5b88b952fc871ff7d7733d78320a404f5fa`  
		Last Modified: Wed, 12 Mar 2025 18:54:26 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0347d31b0c624c67b52d343af6257a98169359944659e9b640543e421d1ac634`  
		Last Modified: Wed, 12 Mar 2025 18:54:26 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca74564b6fbfac8316422985f4bdd2ed1db4503446d8beaaa5746628dfe3838a`  
		Last Modified: Wed, 12 Mar 2025 18:54:32 GMT  
		Size: 83.8 MB (83792574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c9d32aa76df94465ca4cc4ccb7085a9b1343e6e9875e0d94ec7ce7889b93c7`  
		Last Modified: Wed, 12 Mar 2025 18:54:27 GMT  
		Size: 3.9 MB (3858342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
