## `eclipse-temurin:17-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:5abb393ee0a30bd7e9425cc892c6cf18abe9d37fe70c6e321e2af76e709b6cf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2849; amd64
	-	windows version 10.0.17763.6532; amd64

### `eclipse-temurin:17-windowsservercore` - windows version 10.0.20348.2849; amd64

```console
$ docker pull eclipse-temurin@sha256:9c0fad1d7632e9288d575641c62579b1bd968b9c9c1d153420236bd70d4acc44
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2609476645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b967d657dfad2a9df447c71cf234f96a463d05825fba979891d3407c21efbeec`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Thu, 14 Nov 2024 20:17:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 20:17:13 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Thu, 14 Nov 2024 20:17:41 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_x64_windows_hotspot_17.0.13_11.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_x64_windows_hotspot_17.0.13_11.msi ;     Write-Host ('Verifying sha256 (09c8cd1d57681030acfd41105eaf5da2a9721f442cfc9655a3a9a7f382268d94) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '09c8cd1d57681030acfd41105eaf5da2a9721f442cfc9655a3a9a7f382268d94') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 14 Nov 2024 20:17:49 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 14 Nov 2024 20:17:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664c74d4191e99822cddb8db2b3c0a33cc5887d040db693c69d84cdf6adf8a70`  
		Last Modified: Thu, 14 Nov 2024 20:17:52 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7aa5c3313fcb4a5f5ed6899acc950eeb848adbcd4605a2b7517f7960efd05bc`  
		Last Modified: Thu, 14 Nov 2024 20:17:52 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da58cef982c839a6178d91c530d35d84dffffaaf1f4098c16667b5d813b7eaef`  
		Last Modified: Thu, 14 Nov 2024 20:18:06 GMT  
		Size: 356.6 MB (356627709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bbd11fa57c4fc85012f0a14b5453368b27c6d966fa1cc6bfba26d95c3eda56d`  
		Last Modified: Thu, 14 Nov 2024 20:17:52 GMT  
		Size: 360.9 KB (360853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3f2809c14629f1e466d5936cab3b08cf7df562cdcb9e6861b656e650b214fc`  
		Last Modified: Thu, 14 Nov 2024 20:17:52 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-windowsservercore` - windows version 10.0.17763.6532; amd64

```console
$ docker pull eclipse-temurin@sha256:0203af2870ac1d88f47efd209c657dcc4fd837b927747b78d0bebd2fc919469d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2371325708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c9a0cfb650b99ca5877b2998d1a707e9f1e927e92c1bab82fc7606dc1cd45d6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Thu, 14 Nov 2024 20:10:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 20:10:47 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Thu, 14 Nov 2024 20:11:27 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_x64_windows_hotspot_17.0.13_11.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_x64_windows_hotspot_17.0.13_11.msi ;     Write-Host ('Verifying sha256 (09c8cd1d57681030acfd41105eaf5da2a9721f442cfc9655a3a9a7f382268d94) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '09c8cd1d57681030acfd41105eaf5da2a9721f442cfc9655a3a9a7f382268d94') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 14 Nov 2024 20:11:36 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 14 Nov 2024 20:11:36 GMT
CMD ["jshell"]
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
	-	`sha256:1a717e3e87c2134412c33be99d824fb2191e80d342e665ad823db55615ba1504`  
		Last Modified: Thu, 14 Nov 2024 20:11:40 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:029c60d0ef9951ed23115aad8ef330f942bb60287d8e54f15a3c208d91f339ff`  
		Last Modified: Thu, 14 Nov 2024 20:11:41 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f05d06763679c6e545b2c419cba8303476e136729b28bc01700854e4cbaeaf`  
		Last Modified: Thu, 14 Nov 2024 20:11:56 GMT  
		Size: 356.8 MB (356791913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710a07e0c6cc6face5557bd558accb40f0ce061a39d4b22b0f9711460d1f56ae`  
		Last Modified: Thu, 14 Nov 2024 20:11:41 GMT  
		Size: 3.9 MB (3876020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f67f879a20f0654ce5bebd11ff4ba8dbdd1c7ce09889e9067c1493a20466b9`  
		Last Modified: Thu, 14 Nov 2024 20:11:41 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
