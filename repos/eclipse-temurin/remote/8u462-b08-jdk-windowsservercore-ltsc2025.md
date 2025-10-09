## `eclipse-temurin:8u462-b08-jdk-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:1e802bcb6b6cc1455e07cbfaf2ea0e8e885a4a6fe9217227f6d45d60c19417e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `eclipse-temurin:8u462-b08-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull eclipse-temurin@sha256:97d42299757b9c523974461ba0c1b0a8c51a4eb991d3fc356f2e70e6b4ade524
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 GB (3763052838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91f201008c43dcd097de158cd5f6a60814f5f37bc8341cffed82d7c3a97e607d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 10 Sep 2025 21:49:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:49:25 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Wed, 10 Sep 2025 21:49:52 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_windows_hotspot_8u462b08.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_windows_hotspot_8u462b08.msi ;     Write-Host ('Verifying sha256 (6abb1058eb80b3ae13f63cd7aef302724aebaf0a68924fee6a503ff4a0a39901) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '6abb1058eb80b3ae13f63cd7aef302724aebaf0a68924fee6a503ff4a0a39901') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 10 Sep 2025 21:49:58 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b04196491ab7c0d6f4bed7db424ba25e64588b6ff3b36044cbb1ec0d6a415c`  
		Last Modified: Wed, 10 Sep 2025 21:58:36 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de8aabf26da17ff4748169830b29ec13147a6146ff227022277b11153f0a160`  
		Last Modified: Wed, 10 Sep 2025 21:58:36 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83dd8256662d9719014a4406f228588935992a3665ad6241e476009400ebd67e`  
		Last Modified: Wed, 10 Sep 2025 22:19:26 GMT  
		Size: 191.3 MB (191267013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75526bde073191bcd29f28160552cb139f6278a851b920ac6ed03e7a9a69b57d`  
		Last Modified: Wed, 10 Sep 2025 21:58:36 GMT  
		Size: 343.5 KB (343486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
