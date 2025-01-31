## `eclipse-temurin:8u442-b06-jdk-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:1045c012f51c450bfe5850860cd9c1a2d2306cbb884936980a358193a04a46a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:8u442-b06-jdk-windowsservercore` - windows version 10.0.26100.2894; amd64

```console
$ docker pull eclipse-temurin@sha256:76c3aed369b562891cdc97d22e82379ab9d27ca8157c22db1480f36778f03650
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2692075279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b6b6545311cbf4bf46a87b37209404ec68436fb0472f6c29da39f90b9af135e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Fri, 31 Jan 2025 02:17:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Jan 2025 02:17:13 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Fri, 31 Jan 2025 02:17:34 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_windows_hotspot_8u442b06.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_windows_hotspot_8u442b06.msi ;     Write-Host ('Verifying sha256 (fac13d03d3d193509d82ef964060c21f2b20bc0ca3419ecc5cb3ef71283f2f94) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'fac13d03d3d193509d82ef964060c21f2b20bc0ca3419ecc5cb3ef71283f2f94') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 31 Jan 2025 02:17:42 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b960189aaf2d6ccc538da7e09b9ae6f615a77bada8aef25e1d3ff85a533b1f`  
		Last Modified: Fri, 31 Jan 2025 02:17:46 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a71196af466734aa2973a863b990bd2f64de9c4c0d2fb655167e142f13211f`  
		Last Modified: Fri, 31 Jan 2025 02:17:46 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78903cb89d7692d47814c381c39f0e2c845603925fee5f7438b2449d1c186453`  
		Last Modified: Fri, 31 Jan 2025 02:17:56 GMT  
		Size: 191.4 MB (191402599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496df0a47956d61bc1f85579cdac419e17d4399ef5cc5f3fca209be732590013`  
		Last Modified: Fri, 31 Jan 2025 02:17:46 GMT  
		Size: 392.5 KB (392497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u442-b06-jdk-windowsservercore` - windows version 10.0.20348.3091; amd64

```console
$ docker pull eclipse-temurin@sha256:89b828fc4b682e064ea243e16012062dd6cb1d661af24db72dd28eae249e444b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2454092834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c3bba0b036939e8f73f2573f21528ded27143fa860a01a5b22e40ac7bac8a3e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Fri, 31 Jan 2025 01:29:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Jan 2025 01:29:29 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Fri, 31 Jan 2025 01:31:07 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_windows_hotspot_8u442b06.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_windows_hotspot_8u442b06.msi ;     Write-Host ('Verifying sha256 (fac13d03d3d193509d82ef964060c21f2b20bc0ca3419ecc5cb3ef71283f2f94) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'fac13d03d3d193509d82ef964060c21f2b20bc0ca3419ecc5cb3ef71283f2f94') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 31 Jan 2025 01:31:15 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9877880b4b706baf69da2f27306d926c59da2e90f862853c68d43b815a6465dd`  
		Last Modified: Fri, 31 Jan 2025 01:31:19 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15aae7fb37d29751d88118a635a2a75b76220e5049668c28ab76f133cd77ccd3`  
		Last Modified: Fri, 31 Jan 2025 01:31:19 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace0285e8d6429e4b1d4e095752c050b72e1374fa43c4dae5df981912d615517`  
		Last Modified: Fri, 31 Jan 2025 01:31:27 GMT  
		Size: 191.4 MB (191377235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cdaf3bc8474c356c7e1e7b16dbd43a59ffcd94d315eaafc4467c93f24a2957d`  
		Last Modified: Fri, 31 Jan 2025 01:31:19 GMT  
		Size: 327.7 KB (327694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u442-b06-jdk-windowsservercore` - windows version 10.0.17763.6775; amd64

```console
$ docker pull eclipse-temurin@sha256:1bd07b6be36e68c2cb660d387fb989ad3b93c8051ad45cd549a9ce37444dd601
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2313903611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075331b93e71dc32ea19de6237a3e9f4a29e5edb605bc0ebc5382d74cd2ba02c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Fri, 31 Jan 2025 01:29:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Jan 2025 01:29:34 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Fri, 31 Jan 2025 01:31:41 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_windows_hotspot_8u442b06.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_windows_hotspot_8u442b06.msi ;     Write-Host ('Verifying sha256 (fac13d03d3d193509d82ef964060c21f2b20bc0ca3419ecc5cb3ef71283f2f94) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'fac13d03d3d193509d82ef964060c21f2b20bc0ca3419ecc5cb3ef71283f2f94') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 31 Jan 2025 01:31:51 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f3c0eba6a6aa17e79e3b46d76551a81caa76ddea4c521bb137dbc71941746b7`  
		Last Modified: Fri, 31 Jan 2025 01:31:55 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f6208417e0064eac718937ddaade0fe8702e784d11c849907ef9a6c5f1fd87`  
		Last Modified: Fri, 31 Jan 2025 01:31:55 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419584a376dde4b53063ee975c266b5f899f21ed9d5afe64425fa84b824a61f3`  
		Last Modified: Fri, 31 Jan 2025 01:32:04 GMT  
		Size: 191.4 MB (191375021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6431c232e4459898eda409fbee4b3ae6c155e2feb727069a89c62bdc310ab8d`  
		Last Modified: Fri, 31 Jan 2025 01:31:55 GMT  
		Size: 313.8 KB (313781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
