## `eclipse-temurin:23-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:70722d5f87fec4c956a7a8857dcb53923c8a394506b4e648ff9dcb473c20e1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `eclipse-temurin:23-windowsservercore` - windows version 10.0.20348.2762; amd64

```console
$ docker pull eclipse-temurin@sha256:b96a5b1a1e540bd3c4b9584633697e87dfaf1f4c81b144d16c01e4289bede97b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2198161097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d025d6b71858dacdf9041a270133610d0a730662f171df6c330147dca1fc8b8b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Thu, 24 Oct 2024 00:57:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 24 Oct 2024 00:57:53 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Thu, 24 Oct 2024 00:59:28 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_x64_windows_hotspot_23.0.1_11.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_x64_windows_hotspot_23.0.1_11.msi ;     Write-Host ('Verifying sha256 (9ddd8db4b47de9ad2fa1de2db59a5ec2fef891c67eb28cef15c595e8d833ac25) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '9ddd8db4b47de9ad2fa1de2db59a5ec2fef891c67eb28cef15c595e8d833ac25') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-23' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 24 Oct 2024 00:59:35 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 24 Oct 2024 00:59:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5aaa2df4300b7572d62cbbdc39fc51c6d0b0e40dd44599a17622db029fb7cd5`  
		Last Modified: Thu, 24 Oct 2024 00:59:39 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c98720a0cf6ce0b108da139d973fbe1eeb58356fcd61983a0f8722b96302e5e`  
		Last Modified: Thu, 24 Oct 2024 00:59:40 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d04e79115057ebd356ea07775309b91bfdd4457fdcbc3e1309cd0c1e570bc59e`  
		Last Modified: Thu, 24 Oct 2024 00:59:55 GMT  
		Size: 398.5 MB (398489162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65869aba8240e8954e962bec38ff814d8f2fadaf60d32aa80871a21063fc6fce`  
		Last Modified: Thu, 24 Oct 2024 00:59:40 GMT  
		Size: 326.5 KB (326522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6865f8a52a1679cf71d9816f1f376bab55f978f0dfce1cff1cd35758f85c87c4`  
		Last Modified: Thu, 24 Oct 2024 00:59:40 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:23-windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull eclipse-temurin@sha256:dad62b30fffea010a22e48b86fd40c0fd6e14bd32bcdd9d98cb311a52582064e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2304676397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d425395c1365ae2d505285ac96fc6704d924e94155efabc52dd848fa3cda558c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Thu, 24 Oct 2024 00:57:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 24 Oct 2024 00:57:46 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Thu, 24 Oct 2024 00:58:59 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_x64_windows_hotspot_23.0.1_11.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_x64_windows_hotspot_23.0.1_11.msi ;     Write-Host ('Verifying sha256 (9ddd8db4b47de9ad2fa1de2db59a5ec2fef891c67eb28cef15c595e8d833ac25) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '9ddd8db4b47de9ad2fa1de2db59a5ec2fef891c67eb28cef15c595e8d833ac25') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-23' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 24 Oct 2024 00:59:08 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 24 Oct 2024 00:59:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73db80a169c2432c8791ad7fa4a5152f1a9c65f34b0a599005479314580859a`  
		Last Modified: Thu, 24 Oct 2024 00:59:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039efcd4451b0fc286e3de2c6d579c14c72b1d69c64e7fd170fa24f501a9a2c6`  
		Last Modified: Thu, 24 Oct 2024 00:59:12 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe9c36a7877120cfca1828c495c702fca6c64425543d25d6882a0c2ffcd329d`  
		Last Modified: Thu, 24 Oct 2024 00:59:27 GMT  
		Size: 398.5 MB (398500561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af2e8b783a8ce41dfe1ea297ff59d97287cb7ead1b4709e232dbbc86dafeb87`  
		Last Modified: Thu, 24 Oct 2024 00:59:13 GMT  
		Size: 4.3 MB (4346682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3e35eca7f9f75cdd71ea6f5fa2198648e10a5700ce41fe2e1f0840113fc712`  
		Last Modified: Thu, 24 Oct 2024 00:59:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
