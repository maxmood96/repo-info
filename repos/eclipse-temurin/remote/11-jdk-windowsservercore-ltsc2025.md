## `eclipse-temurin:11-jdk-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:56c3bfe7a7ceeae61abeacb9290ecf95635f553f4bed88585dbd95a6280c7931
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `eclipse-temurin:11-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.32522; amd64

```console
$ docker pull eclipse-temurin@sha256:1ac8d0f59c21333a0d75a823f1d7b4bd3576236d7c597d4deb81eadc2c1f7ff3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2451368790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ff38efbad591f86143eae1f61f45ec3f447127bc5a1be50f12a82cef85d3d5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Tue, 10 Mar 2026 21:57:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Mar 2026 21:57:42 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Tue, 10 Mar 2026 21:58:16 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_windows_hotspot_11.0.30_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_windows_hotspot_11.0.30_7.msi ;     Write-Host ('Verifying sha256 (5a7e985d6e89c864cf176c9ebf919ab1e97b40877b8e5290e4c51f532e37d1c2) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '5a7e985d6e89c864cf176c9ebf919ab1e97b40877b8e5290e4c51f532e37d1c2') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 10 Mar 2026 21:58:22 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 10 Mar 2026 21:58:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4044d53eb07512e97add181612306692edbb0e2fead4607122de49f8a263823`  
		Last Modified: Tue, 10 Mar 2026 21:58:26 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12f6ee8f67a6572cacc81a8b032193083fd2bc54d209df1afc3e33cc79e53edc`  
		Last Modified: Tue, 10 Mar 2026 21:58:26 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18410a66b6d6b96daf2e1f48f28cda0df459a97d4b155444cf5ae1a5d862b4cf`  
		Last Modified: Tue, 10 Mar 2026 21:58:45 GMT  
		Size: 369.8 MB (369811280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781c629d16a79ef9442b934c84e86c03758dd78fb4bc8345ebbc0791bdf61d53`  
		Last Modified: Tue, 10 Mar 2026 21:58:26 GMT  
		Size: 357.6 KB (357578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aeea95f427530e77f1c91d08f3ef20baab993b9598b05451533a2069134e5e5`  
		Last Modified: Tue, 10 Mar 2026 21:58:26 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
