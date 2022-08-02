## `eclipse-temurin:18-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:3afe20cb4ebb8c64e8472510e63878ddd51f1603b613d34d2db6119915455b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.825; amd64

### `eclipse-temurin:18-windowsservercore-ltsc2022` - windows version 10.0.20348.825; amd64

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
