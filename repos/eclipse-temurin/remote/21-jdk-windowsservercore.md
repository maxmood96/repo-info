## `eclipse-temurin:21-jdk-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:8aeb8a46c67c854d81ad2279104a82bdb4564562348d90bda916b31eacb9eadc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `eclipse-temurin:21-jdk-windowsservercore` - windows version 10.0.20348.3207; amd64

```console
$ docker pull eclipse-temurin@sha256:c5ff6818fa5f49d6682d923db9ccbd4c26ad0b351bd7cd49ecaf0329d059787d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2644458092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e15987855ba6632322c7e301a46aa70717db1180517c53546a6512e53a83b4f8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:38:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:38:40 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 13 Feb 2025 00:39:11 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_windows_hotspot_21.0.6_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_windows_hotspot_21.0.6_7.msi ;     Write-Host ('Verifying sha256 (c361f8a018cffdad1ad0a0ce3e5032fc7314dec3f73642dc626a6121d487008b) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'c361f8a018cffdad1ad0a0ce3e5032fc7314dec3f73642dc626a6121d487008b') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 13 Feb 2025 00:39:19 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:39:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5337aac2f734a6eaedbf6a43b2ce7bd06c29336974f2c9236f474a9984019d5e`  
		Last Modified: Thu, 13 Feb 2025 00:39:22 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4eb44763b445150a43fbe85a9fc25387710671be37d10f0514021bd2f0c53e2`  
		Last Modified: Thu, 13 Feb 2025 00:39:22 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da4043fa2f3d082303ffc9364a6325f55b6e66bf86bb4bbcd5c24cc4b4e94fb`  
		Last Modified: Thu, 13 Feb 2025 00:39:38 GMT  
		Size: 380.2 MB (380247163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:523d170d3a19282101db9d70453ab049f68b7548c79b4010001c79c5a1385386`  
		Last Modified: Thu, 13 Feb 2025 00:39:22 GMT  
		Size: 349.1 KB (349066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d9c776182388bf5991c63a752fdcd2620dd2efc45145f69bf8bba7f3bb594a`  
		Last Modified: Thu, 13 Feb 2025 00:39:22 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jdk-windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull eclipse-temurin@sha256:2b341a2284526a2093c4befe19cccea553b2450e18b1e53848c9c2c71eec052e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2521232441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1a53e976b7b7737c3065d4fdfb21d8b06e8f51fc080c2922c1f6b145b4ad617`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:34:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:34:46 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 13 Feb 2025 00:35:42 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_windows_hotspot_21.0.6_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_windows_hotspot_21.0.6_7.msi ;     Write-Host ('Verifying sha256 (c361f8a018cffdad1ad0a0ce3e5032fc7314dec3f73642dc626a6121d487008b) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'c361f8a018cffdad1ad0a0ce3e5032fc7314dec3f73642dc626a6121d487008b') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 13 Feb 2025 00:35:51 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:35:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20e81ad74c5929090ba1ae03cc0c47e6ccf3e288b34a38da32d00988d4fa282`  
		Last Modified: Thu, 13 Feb 2025 00:35:55 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35520a9e47699dc0013d8c97152f29b19ee91251e371e22c3c4e968cb64660ec`  
		Last Modified: Thu, 13 Feb 2025 00:35:55 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d0b4d731e94d619a7552f0496b63080e3980a8b1fb21953217a1143c5c5fd1`  
		Last Modified: Thu, 13 Feb 2025 00:36:10 GMT  
		Size: 380.3 MB (380258866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:483029b5a94b0f5f85b7bb095e4ebe725d0aa9db448fde156bb54e3c22ae20ac`  
		Last Modified: Thu, 13 Feb 2025 00:35:56 GMT  
		Size: 4.1 MB (4060909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d4bdf556a9ab8cd0372deaf4928318d8aaaf86ca1b7e89e8caa6d6a78039cd`  
		Last Modified: Thu, 13 Feb 2025 00:35:55 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
