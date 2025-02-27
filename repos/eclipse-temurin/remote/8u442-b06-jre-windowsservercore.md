## `eclipse-temurin:8u442-b06-jre-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:579cf83d8c779b2f1d3168b242cddd83eb580cab37e61395f624b184cdf219cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `eclipse-temurin:8u442-b06-jre-windowsservercore` - windows version 10.0.20348.3207; amd64

```console
$ docker pull eclipse-temurin@sha256:b11219b6f7cfb669eb078ab09533d8094c0b6e0b05ccca211be84072639e614f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2337002969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1907942923176ac03b3b11eae607f3a32d48bf81438ca8ae7b7ac1c6abd857d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:34:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:34:23 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 13 Feb 2025 00:34:40 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_x64_windows_hotspot_8u442b06.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_x64_windows_hotspot_8u442b06.msi ;     Write-Host ('Verifying sha256 (4dd03622b9690427dbcd6df6c60eb6e1a422f1eb7389f0d08ef844bf43e23eab) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '4dd03622b9690427dbcd6df6c60eb6e1a422f1eb7389f0d08ef844bf43e23eab') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 13 Feb 2025 00:34:45 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
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
	-	`sha256:709de2d7baa2b5ff04c5811e124a3822f82bc8fdb399cbbe9fc20d6062d3b8ee`  
		Last Modified: Thu, 13 Feb 2025 00:34:49 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe391c0a46d2691d0547a2cfacaf1ba99649581c1f0a7b98b55e1f7cf931eb53`  
		Last Modified: Thu, 13 Feb 2025 00:34:49 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c265b182c0bd325f961bcde1f079dec78555c29529cec55f05d61268dbf97d`  
		Last Modified: Thu, 13 Feb 2025 00:34:54 GMT  
		Size: 72.8 MB (72770890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f36363a808151b4a4fb7269acd025faabf53abbe3a96c177bdbe443e775dfc17`  
		Last Modified: Thu, 13 Feb 2025 00:34:50 GMT  
		Size: 371.5 KB (371468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u442-b06-jre-windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull eclipse-temurin@sha256:05047ddf9c17f5bf507acd1279cb0fc82300ced707698aababa1f7962a0565ce
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2210009999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a91ed06d3d3add1d13d6109b95e998ba23b8c81c4367714d8cd0e1f14af33a1f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:35:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:35:44 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 13 Feb 2025 00:36:32 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_x64_windows_hotspot_8u442b06.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_x64_windows_hotspot_8u442b06.msi ;     Write-Host ('Verifying sha256 (4dd03622b9690427dbcd6df6c60eb6e1a422f1eb7389f0d08ef844bf43e23eab) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '4dd03622b9690427dbcd6df6c60eb6e1a422f1eb7389f0d08ef844bf43e23eab') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 13 Feb 2025 00:36:39 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
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
	-	`sha256:6ac69076983376ff629663e766e7db51a84f525970e7586ad1f8e5f6b7e303b1`  
		Last Modified: Thu, 13 Feb 2025 00:36:41 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c564b9eec5d35f7c007a9fa54b952cde7038b03f44c66a780fac6d36dc77d428`  
		Last Modified: Thu, 13 Feb 2025 00:36:42 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1003659653f4f619042718995c308184b09da793ff15a417d87ad50a3f4e956b`  
		Last Modified: Thu, 13 Feb 2025 00:36:46 GMT  
		Size: 72.8 MB (72759679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc9305de9c4599ce5fb9e2004e6bf13820240655d277f0f57e4f884173f1b59`  
		Last Modified: Thu, 13 Feb 2025 00:36:41 GMT  
		Size: 338.9 KB (338940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
