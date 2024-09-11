## `eclipse-temurin:22-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:cdb27439314efc2026b2bc15fc2fb9aaee594e895565c8921a1006148713dc4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `eclipse-temurin:22-windowsservercore` - windows version 10.0.20348.2700; amd64

```console
$ docker pull eclipse-temurin@sha256:90df635aeaad6b85a49db30691d419af3447b3e54f723649efc864c52d2d6925
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1840680278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cecad6e536f742617f3cde3bc9173759aa039753acf32c146d47dbc48a0f467`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 11 Sep 2024 00:35:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 00:59:58 GMT
ENV JAVA_VERSION=jdk-22.0.2+9
# Wed, 11 Sep 2024 01:00:45 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_x64_windows_hotspot_22.0.2_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_x64_windows_hotspot_22.0.2_9.msi ;     Write-Host ('Verifying sha256 (d961cb2e612223e94b0506c61e1360d11b8961eab822ff12fa9b8921c4627a25) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'd961cb2e612223e94b0506c61e1360d11b8961eab822ff12fa9b8921c4627a25') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-22' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 11 Sep 2024 01:01:03 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 11 Sep 2024 01:01:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e0ff9a79ca5aec0b3e3be0c49c873a237847a9d74342acad1818e3f10647107`  
		Last Modified: Wed, 11 Sep 2024 01:13:29 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d58ba21cab3ac9d3120e7a871ec58aa53c0b919591d4e76d24f776882ac1ef8`  
		Last Modified: Wed, 11 Sep 2024 01:30:40 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29ba654f7f247ae0539ee48fba80dac459e8ae4995313e8c5cea439f5b6af58`  
		Last Modified: Wed, 11 Sep 2024 01:31:05 GMT  
		Size: 378.2 MB (378211830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29bffe1f7dc358732f14b30ba60be8c48194d13abf2c95f74b19f0957a4da5e`  
		Last Modified: Wed, 11 Sep 2024 01:30:40 GMT  
		Size: 271.8 KB (271824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0732e5f32723c7990517aabb4dc393ef962d2e0afb0d9f74c5cf5b17abb7295`  
		Last Modified: Wed, 11 Sep 2024 01:30:40 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:22-windowsservercore` - windows version 10.0.17763.6293; amd64

```console
$ docker pull eclipse-temurin@sha256:2348a2d4b50c9cc14fea6ea2715291a3f17c75784af35c59da7c4dbbb8c28ada
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2102534793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13462a1bc2bea2130c10003fa39f4827c7acb8b51a09856193463057cc76322d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 00:36:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 01:01:11 GMT
ENV JAVA_VERSION=jdk-22.0.2+9
# Wed, 11 Sep 2024 01:01:59 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_x64_windows_hotspot_22.0.2_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_x64_windows_hotspot_22.0.2_9.msi ;     Write-Host ('Verifying sha256 (d961cb2e612223e94b0506c61e1360d11b8961eab822ff12fa9b8921c4627a25) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'd961cb2e612223e94b0506c61e1360d11b8961eab822ff12fa9b8921c4627a25') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-22' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 11 Sep 2024 01:02:20 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 11 Sep 2024 01:02:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b681a22e2ab818abdc55dff7075266cbdad9e0c1d79f16a962cabde9559b4bc1`  
		Last Modified: Wed, 11 Sep 2024 01:17:09 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824dd5e8f7c52e0ad1e1a65c8241f51cc7f3b98836382cb53411e025efa7aabb`  
		Last Modified: Wed, 11 Sep 2024 01:31:15 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e49275d1c8393111478dca0dc0e531438594c0e0b57cb2efe91225eb7390ccc`  
		Last Modified: Wed, 11 Sep 2024 01:31:39 GMT  
		Size: 378.2 MB (378239939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cccf1f6c4a93948cc80ffd339c8becd16d2a1ce3b608cc538c40902df7af62a5`  
		Last Modified: Wed, 11 Sep 2024 01:31:16 GMT  
		Size: 4.0 MB (4022285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7e4caa38a9dd707f7efe8bfd5ee54cbfdfee6cf5f98b18274532c60a57168c`  
		Last Modified: Wed, 11 Sep 2024 01:31:15 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
