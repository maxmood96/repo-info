## `eclipse-temurin:23-jre-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:92c0ddac31ebc87b5ba6872b5d1e56309a93e3be21fa6b8e69e394ea3e94c4f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `eclipse-temurin:23-jre-windowsservercore` - windows version 10.0.26100.3476; amd64

```console
$ docker pull eclipse-temurin@sha256:5c84ae4a2983906afccac7252ba121fc6ec9f48fc2506a643892c61fae534cc0
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2992856171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:156f65746c28722b1c5ddaacce01c1995b655023199edded2db198ab8cbb0536`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Wed, 12 Mar 2025 18:48:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:48:32 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Wed, 12 Mar 2025 18:48:50 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_x64_windows_hotspot_23.0.2_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_x64_windows_hotspot_23.0.2_7.msi ;     Write-Host ('Verifying sha256 (07ddf8b8d004692261d0ab769a31176abd22b5203cee44317328f9113a99e486) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '07ddf8b8d004692261d0ab769a31176abd22b5203cee44317328f9113a99e486') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-23' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Mar 2025 18:49:00 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30bda975cec39746fd9bb443f769168852b25ac39d5b8ae30407b22a5db2e1f4`  
		Last Modified: Wed, 12 Mar 2025 18:49:04 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23bbcb35f9d6c12806eddea94c9b7e7cc624d5e380bd65cf1eccc942a678a1a0`  
		Last Modified: Wed, 12 Mar 2025 18:49:04 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9abd76daef23056ceaf226a3967453d32deb3930945effe1c6a204bf1ce3dacf`  
		Last Modified: Wed, 12 Mar 2025 18:49:11 GMT  
		Size: 83.8 MB (83824626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63445a3a0de03ee14132199eccfbd773d5361a02a634bbc10feef74e8785e2c7`  
		Last Modified: Wed, 12 Mar 2025 18:49:04 GMT  
		Size: 381.2 KB (381212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:23-jre-windowsservercore` - windows version 10.0.20348.3328; amd64

```console
$ docker pull eclipse-temurin@sha256:67ead36058db938d6d9a1046ea1ab298882c0c7bdadd2c6b2b714377c9c46650
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2354081310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8c6bdf1e340831b6b9879cce4fef22f2f84abc0961f30b508f54fc2075242bb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Wed, 12 Mar 2025 18:47:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:47:51 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Wed, 12 Mar 2025 18:48:09 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_x64_windows_hotspot_23.0.2_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_x64_windows_hotspot_23.0.2_7.msi ;     Write-Host ('Verifying sha256 (07ddf8b8d004692261d0ab769a31176abd22b5203cee44317328f9113a99e486) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '07ddf8b8d004692261d0ab769a31176abd22b5203cee44317328f9113a99e486') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-23' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Mar 2025 18:48:15 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef7e8e2bed9dc462552ee7b66af412f94af6edcbb4445ccf1a915a027aa72c0c`  
		Last Modified: Wed, 12 Mar 2025 18:48:19 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff699b9b8dae71e47bdb27510af2e21aafe47a9e762cb85cc1971601e1ebbde5`  
		Last Modified: Wed, 12 Mar 2025 18:48:19 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3045a404a8c63ea0ed6acc19b017630523bf5d263802fe677a95f283cabe4e7`  
		Last Modified: Wed, 12 Mar 2025 18:48:26 GMT  
		Size: 83.8 MB (83788538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd25b24a92e16bf231a90d7248e8597ee4738c9c74b5de3c7946210b70da26a`  
		Last Modified: Wed, 12 Mar 2025 18:48:19 GMT  
		Size: 349.0 KB (349013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:23-jre-windowsservercore` - windows version 10.0.17763.7009; amd64

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
