## `eclipse-temurin:23-jdk-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:b53f8829d130657c937ddf0b0d163f3e5e7015fbe48627063998e762d9ddf647
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2849; amd64

### `eclipse-temurin:23-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.2849; amd64

```console
$ docker pull eclipse-temurin@sha256:ffb3ea23ea0e3bd304d4b2f045a44315ace6c6bf24bb2160aca002dc830325ab
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2651218704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c505e95960253cdd390c11cfb7499052fd716f6a386adb1dd695c0d93fba9fc5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Thu, 14 Nov 2024 20:23:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 20:23:46 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Thu, 14 Nov 2024 20:24:22 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_x64_windows_hotspot_23.0.1_11.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_x64_windows_hotspot_23.0.1_11.msi ;     Write-Host ('Verifying sha256 (9ddd8db4b47de9ad2fa1de2db59a5ec2fef891c67eb28cef15c595e8d833ac25) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '9ddd8db4b47de9ad2fa1de2db59a5ec2fef891c67eb28cef15c595e8d833ac25') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-23' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 14 Nov 2024 20:24:31 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 14 Nov 2024 20:24:32 GMT
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
	-	`sha256:946ce697892d637659f9caa23eb1c0076700570d13fa5f2f78e191a66e2ff723`  
		Last Modified: Thu, 14 Nov 2024 20:24:35 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd6e7fec1fb0d449750a6308df0d762f0801470755471003aa4b5a05384e739`  
		Last Modified: Thu, 14 Nov 2024 20:24:35 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e12740804ee806d4665752765bdbf14737e29eea3fdbe8ef4b922e37f08e947`  
		Last Modified: Thu, 14 Nov 2024 20:24:51 GMT  
		Size: 398.4 MB (398366223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286f67bc5699a9a0f962b996ce42a735e98737e9293e1654ad54792e4f10b0c5`  
		Last Modified: Thu, 14 Nov 2024 20:24:35 GMT  
		Size: 364.4 KB (364396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63206d29332caa68879a7b1012d214787cf67aecf15f437b404de8ebae03e98`  
		Last Modified: Thu, 14 Nov 2024 20:24:35 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
