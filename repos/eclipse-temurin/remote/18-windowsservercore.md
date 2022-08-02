## `eclipse-temurin:18-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:c982fabed85279ff2d69a6bb315ccd58b04f7bea3f23d8ce82cf050e9ee43f62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.825; amd64
	-	windows version 10.0.17763.3165; amd64

### `eclipse-temurin:18-windowsservercore` - windows version 10.0.20348.825; amd64

```console
$ docker pull eclipse-temurin@sha256:525d2b99cff7acc46a32d875aecc54ed6aeb02ca0988046e776b42017be719b6
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2655982725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490929cc43480ce1c2f4d4a8f9f2d26600c7f84365edc4cd341725275c983860`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Mon, 04 Jul 2022 17:46:55 GMT
RUN Install update 10.0.20348.825
# Tue, 12 Jul 2022 19:25:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Aug 2022 18:26:50 GMT
ENV JAVA_VERSION=jdk-18.0.2+9
# Tue, 02 Aug 2022 18:27:58 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_x64_windows_hotspot_18.0.2_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_x64_windows_hotspot_18.0.2_9.msi ;     Write-Host ('Verifying sha256 (b3f9fd4f94e9f117387de4ecbfaf0903a93e64c39683236acba583e75d41ba07) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'b3f9fd4f94e9f117387de4ecbfaf0903a93e64c39683236acba583e75d41ba07') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-18' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 02 Aug 2022 18:28:22 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 02 Aug 2022 18:28:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e1a27cb9d4615dec325f2cbabac4ca1f65413bdbb8b440cc961df032993a9b81`  
		Size: 863.4 MB (863367943 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6452cb934201756f0ed9fb5e0cbea54a22a66412cb696ff30a1923d456e28bcf`  
		Last Modified: Tue, 12 Jul 2022 20:20:48 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc14bd69273eb440f31c9bab8b8c19bdde6f079401e43e46ed1bce8dd0b6700b`  
		Last Modified: Tue, 02 Aug 2022 18:44:13 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c435a17a131963ac4a1f906f61e2959bc40a2c158be7baa55e477bc11e46e1`  
		Last Modified: Tue, 02 Aug 2022 18:44:46 GMT  
		Size: 355.2 MB (355175778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3020a6e5923cafcbbdcd52fd544421ddb76c679ab20e70a58f3b266e1b88f389`  
		Last Modified: Tue, 02 Aug 2022 18:44:14 GMT  
		Size: 571.1 KB (571089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e097f5f6618859130cc3c08f376460ddb453a3446130b2733bd579c09386b50b`  
		Last Modified: Tue, 02 Aug 2022 18:44:13 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:18-windowsservercore` - windows version 10.0.17763.3165; amd64

```console
$ docker pull eclipse-temurin@sha256:c172f52e0f689a18a73c4f3463665df91235de1e11f33696e364bb0aa9d12266
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3030787775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:614b83368286d2d780efa6e3ee4d6ec74bb57399ea1f33f7efc4eea7b7ea9c0f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Wed, 06 Jul 2022 22:37:15 GMT
RUN Install update 10.0.17763.3165
# Tue, 12 Jul 2022 19:32:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Aug 2022 18:28:32 GMT
ENV JAVA_VERSION=jdk-18.0.2+9
# Tue, 02 Aug 2022 18:30:07 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_x64_windows_hotspot_18.0.2_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_x64_windows_hotspot_18.0.2_9.msi ;     Write-Host ('Verifying sha256 (b3f9fd4f94e9f117387de4ecbfaf0903a93e64c39683236acba583e75d41ba07) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'b3f9fd4f94e9f117387de4ecbfaf0903a93e64c39683236acba583e75d41ba07') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-18' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 02 Aug 2022 18:31:07 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 02 Aug 2022 18:31:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7aca8de30754f19fe03ee4c21eed0762efb5e91bf684b0cc36cc92b2af13446d`  
		Size: 794.9 MB (794877652 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:912efe6370f7047e630e1f70d9201e3143571e3ed1fe50a1e61754d2d536ea95`  
		Last Modified: Tue, 12 Jul 2022 20:21:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f4de99d54b8fbebc1ba4c25840e27b3a1810a5cdb487374ce99f80bca2e4ab`  
		Last Modified: Tue, 02 Aug 2022 18:45:00 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01dcef63167b78c84a860a0748243a8c6e637d2bab23b8940635b0694e70fdc`  
		Last Modified: Tue, 02 Aug 2022 18:45:27 GMT  
		Size: 354.9 MB (354928906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae33442a80836a46049f0bfa52f736f6fb2e88150f8c201a85b450607922ea77`  
		Last Modified: Tue, 02 Aug 2022 18:45:00 GMT  
		Size: 3.8 MB (3810870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32763909af62233c821fa026b94187e2318cddc9ec047ca713ea1b8e0a0865a5`  
		Last Modified: Tue, 02 Aug 2022 18:45:00 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
