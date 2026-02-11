## `eclipse-temurin:17-jdk-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:26d96ead943587c5cc395a1c1160f9abded7de10f44097cc6829e13a5219ccd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32370; amd64
	-	windows version 10.0.20348.4773; amd64

### `eclipse-temurin:17-jdk-windowsservercore` - windows version 10.0.26100.32370; amd64

```console
$ docker pull eclipse-temurin@sha256:51042aa95c10446cfe073af7f0df6baff9e494a13fa8522d91473b85c22938ad
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2320766948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bfa8067ca725f59f6336a133ac58c8d96165afb90ad2915352676f8832ecbb7`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Feb 2026 22:21:49 GMT
RUN Install update 10.0.26100.32370
# Tue, 10 Feb 2026 22:53:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Feb 2026 22:53:50 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 10 Feb 2026 22:54:16 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_windows_hotspot_17.0.18_8.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_windows_hotspot_17.0.18_8.msi ;     Write-Host ('Verifying sha256 (bd169b6b8439e1d715eff789e355029e222ce6152994cefc3e666783ade8ff44) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'bd169b6b8439e1d715eff789e355029e222ce6152994cefc3e666783ade8ff44') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 10 Feb 2026 22:54:21 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 10 Feb 2026 22:54:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456534216d0c12d9314cda831989d54bb3f542d7d43d9772ba40654db6dbd7bc`  
		Last Modified: Tue, 10 Feb 2026 18:52:01 GMT  
		Size: 441.7 MB (441700471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef73c96d3477d0e2f9c37003a22dd33fc423f4633c667bc514de5bc85c477e7`  
		Last Modified: Tue, 10 Feb 2026 22:54:26 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ebb2a5a3cb7c39e71540fc3f7d16f61f3c97cd4ccaaab95105c57850dc453d`  
		Last Modified: Tue, 10 Feb 2026 22:54:26 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b57d05317778c9986dee38339f51fa97cb7d06162b1ceaf7ecf38a03c70e4372`  
		Last Modified: Tue, 10 Feb 2026 22:54:44 GMT  
		Size: 355.6 MB (355642771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06954731122884a13fb1924be78b2d0514c8185b5bf5ee3710a2061c6c5c042c`  
		Last Modified: Tue, 10 Feb 2026 22:54:26 GMT  
		Size: 360.4 KB (360373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51bf18bc3fd161e22171d9b184535d1b622521e8aa73192f2e429121b518ca43`  
		Last Modified: Tue, 10 Feb 2026 22:54:26 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jdk-windowsservercore` - windows version 10.0.20348.4773; amd64

```console
$ docker pull eclipse-temurin@sha256:e8a0201e806b03acb05ee36aa876049990003ea80c75922a48e50961522023ac
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2218647902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aea94ae731e65b533a7a99191ff729926f63337060c71a020ce8df9d31e8af33`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Tue, 10 Feb 2026 22:52:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Feb 2026 23:01:12 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 10 Feb 2026 23:01:52 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_windows_hotspot_17.0.18_8.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_windows_hotspot_17.0.18_8.msi ;     Write-Host ('Verifying sha256 (bd169b6b8439e1d715eff789e355029e222ce6152994cefc3e666783ade8ff44) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'bd169b6b8439e1d715eff789e355029e222ce6152994cefc3e666783ade8ff44') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 10 Feb 2026 23:01:59 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 10 Feb 2026 23:01:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a1a68b70a6037a04683b570a391289e218225652d139b4c315a66941376ca1`  
		Last Modified: Tue, 10 Feb 2026 22:54:47 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0cc5a2781a6adae6daa7e965b72e3ce6ef19d84dc1bef551fe3036e5c4c1e7`  
		Last Modified: Tue, 10 Feb 2026 23:02:03 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40e7a1ecf3b2540f8065e165b52da9b1e7a847c13379d99e32734141552e9fb`  
		Last Modified: Tue, 10 Feb 2026 23:02:21 GMT  
		Size: 355.6 MB (355634248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553646bc5dc36c98bb99104aea41fd2d26e4c82f7c57a22ed1b5c429cc2d2b18`  
		Last Modified: Tue, 10 Feb 2026 23:02:03 GMT  
		Size: 352.5 KB (352534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea13e748d4d1cde6e8a86baea25108b790d1cf48d173252cf33ae4ed5db58f26`  
		Last Modified: Tue, 10 Feb 2026 23:02:03 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
