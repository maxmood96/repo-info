## `eclipse-temurin:11-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:73b01784e27133a951e9e304f09b023e9f0d4d8a0884edc040126a622fac12dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1906; amd64
	-	windows version 10.0.17763.4737; amd64

### `eclipse-temurin:11-windowsservercore` - windows version 10.0.20348.1906; amd64

```console
$ docker pull eclipse-temurin@sha256:6f61f652b7318bec14818d46ed42aa3c0d22ec0ed225d50d9fcbf22b05b4c446
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2165051706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbe2fe102086adee7018bb82722e5a1b195932dda96c8e9f09875239d3c360bf`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 03 Aug 2023 10:01:10 GMT
RUN Install update 10.0.20348.1906
# Wed, 09 Aug 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Aug 2023 23:44:26 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Wed, 09 Aug 2023 23:45:27 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_x64_windows_hotspot_11.0.20_8.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_x64_windows_hotspot_11.0.20_8.msi ;     Write-Host ('Verifying sha256 (ff55a265c41cc2525f87dd3790f469a074a5e196c2354c28a9f553420bdc4468) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'ff55a265c41cc2525f87dd3790f469a074a5e196c2354c28a9f553420bdc4468') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 09 Aug 2023 23:45:47 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 09 Aug 2023 23:45:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a441455ace20af58f01367d769afc2b25c3db3e4a7aee67a634d14826f6f19`  
		Last Modified: Tue, 08 Aug 2023 18:20:41 GMT  
		Size: 408.8 MB (408765102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53d0f5bc5dd4cb7976f788ee32f7195b84c7964cb22bc38a49eb55673629149`  
		Last Modified: Thu, 10 Aug 2023 00:18:32 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b34c01365a0fadb8fbed107ee7573477725430a635f066146a4d5e08680ffb`  
		Last Modified: Thu, 10 Aug 2023 00:22:20 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d15d9f9c9e772d95befe3a5290151c6d03484c76980689e5ebbd415c84f560`  
		Last Modified: Thu, 10 Aug 2023 00:22:48 GMT  
		Size: 367.4 MB (367405398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f17522eea38b2e6182c4b4513eab7fee165997abf341ba4574b52395e27bf9`  
		Last Modified: Thu, 10 Aug 2023 00:22:20 GMT  
		Size: 278.4 KB (278427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e8b17ed76736a2ab73f47d4fbb1b76b0b0409b9ad31fcb7175fe049dfb2c60`  
		Last Modified: Thu, 10 Aug 2023 00:22:20 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-windowsservercore` - windows version 10.0.17763.4737; amd64

```console
$ docker pull eclipse-temurin@sha256:6ce14c811edeea15d6b3912b719080ca02d5b79bf0e14c31ce5a9010db66952d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2363616357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d067ee3e90b23837584f52008d27f19cafedfd834caf7ef495bf5ced953e10`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 02 Aug 2023 09:07:15 GMT
RUN Install update 10.0.17763.4737
# Wed, 09 Aug 2023 23:36:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Aug 2023 23:45:55 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Wed, 09 Aug 2023 23:47:30 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_x64_windows_hotspot_11.0.20_8.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_x64_windows_hotspot_11.0.20_8.msi ;     Write-Host ('Verifying sha256 (ff55a265c41cc2525f87dd3790f469a074a5e196c2354c28a9f553420bdc4468) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'ff55a265c41cc2525f87dd3790f469a074a5e196c2354c28a9f553420bdc4468') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 09 Aug 2023 23:48:29 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 09 Aug 2023 23:48:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95f433aa7d90194e65f6b08a599b3ee12292e124d47c204107baedfd71054c1`  
		Last Modified: Tue, 08 Aug 2023 18:31:16 GMT  
		Size: 345.3 MB (345334986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03d23fbbd4f650b6f60106a3cc28d711efce2f97cfb80b67e2dec305e011aa3`  
		Last Modified: Thu, 10 Aug 2023 00:19:47 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f8f808e2a3e4ee989247978524a9ace6dc1fca713ef87f35c45bc6a5271ba5`  
		Last Modified: Thu, 10 Aug 2023 00:23:01 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464eaddfdba6437bf8498c48cb1f387656ae6e6461109a478530d8366c9ba728`  
		Last Modified: Thu, 10 Aug 2023 00:23:28 GMT  
		Size: 367.4 MB (367432812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9ebf3a6b40763ff2fa3eb71b0f1612995d7c8955b6dac4abc28800a44d7cb63`  
		Last Modified: Thu, 10 Aug 2023 00:23:01 GMT  
		Size: 224.2 KB (224206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e11b66e95b64f23ca263d3458ef37b1dd3b4a94f8b13b339e14105a274066515`  
		Last Modified: Thu, 10 Aug 2023 00:23:01 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
