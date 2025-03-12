## `eclipse-temurin:21-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:f5535f4d946195df17871183a57b73a9ae07fa76f25018d5e66968ecbf821fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `eclipse-temurin:21-windowsservercore` - windows version 10.0.26100.3476; amd64

```console
$ docker pull eclipse-temurin@sha256:e1556e55dd6d8ce6a9702347ec571b589aa71b65948f5d0647594e9f58a79d17
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3289317412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ed0264f4fea478d53e23fcbccec7593f02b5afe4949667ba80b23932bf6c109`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Wed, 12 Mar 2025 18:48:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:48:19 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Wed, 12 Mar 2025 18:48:45 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_windows_hotspot_21.0.6_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_windows_hotspot_21.0.6_7.msi ;     Write-Host ('Verifying sha256 (c361f8a018cffdad1ad0a0ce3e5032fc7314dec3f73642dc626a6121d487008b) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'c361f8a018cffdad1ad0a0ce3e5032fc7314dec3f73642dc626a6121d487008b') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Mar 2025 18:48:53 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:48:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df8daf6a650f2bc06e062c5cec319d9210ed269c0556597ccd6343764604993`  
		Last Modified: Wed, 12 Mar 2025 18:48:58 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8388d3eaaa5368118865dc0540c29759901dd1187dff19fff95fc41f32167f5`  
		Last Modified: Wed, 12 Mar 2025 18:48:57 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b8417d3f7cd49ece52c6f08cba2771c21a05675ffeb0025ef91f9dd6f07093`  
		Last Modified: Wed, 12 Mar 2025 18:49:16 GMT  
		Size: 380.3 MB (380284999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b32c1b47df85e2abd6df5fdb689ba4d335d5a23cb54b2aac8b6ad9fb7dd2caf4`  
		Last Modified: Wed, 12 Mar 2025 18:48:58 GMT  
		Size: 380.7 KB (380711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:028f273bc09dd24e62d1b347f4c0480746d8ec8967eb002e49fbedb75196a01a`  
		Last Modified: Wed, 12 Mar 2025 18:48:58 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-windowsservercore` - windows version 10.0.20348.3328; amd64

```console
$ docker pull eclipse-temurin@sha256:e5c7d1189b3ee4d41164b4390d992186100158edab3109349ebc43e1d8887d49
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2650564131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca8f8555e0be91aefdcfd793882dd73b73c09088ba2d5c077880ac7fce8be61`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Wed, 12 Mar 2025 18:53:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:53:11 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Wed, 12 Mar 2025 18:53:43 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_windows_hotspot_21.0.6_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_windows_hotspot_21.0.6_7.msi ;     Write-Host ('Verifying sha256 (c361f8a018cffdad1ad0a0ce3e5032fc7314dec3f73642dc626a6121d487008b) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'c361f8a018cffdad1ad0a0ce3e5032fc7314dec3f73642dc626a6121d487008b') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Mar 2025 18:53:51 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:53:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0163a3a9db34e00c4ec45361724c6a5fe817605d64eefde8f45b4e277531b9fb`  
		Last Modified: Wed, 12 Mar 2025 18:53:54 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b65fde05e6a60bc5337fda575667d42fdb84e71d4268437ca069ff0060e983`  
		Last Modified: Wed, 12 Mar 2025 18:53:54 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665199222afe9274e2bbc3ea782642908b72934088c19cb2f4c078c33eed1387`  
		Last Modified: Wed, 12 Mar 2025 18:54:11 GMT  
		Size: 380.3 MB (380259594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c454d7f75a8e2baed19b3d8bff04782685bcfb9dd2920f8e2615185ecc47e6`  
		Last Modified: Wed, 12 Mar 2025 18:53:55 GMT  
		Size: 359.5 KB (359481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10437759ee64227eb5709dc6bb49647dec751c2f46f7957020b5ee6c9177a711`  
		Last Modified: Wed, 12 Mar 2025 18:53:54 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-windowsservercore` - windows version 10.0.17763.7009; amd64

```console
$ docker pull eclipse-temurin@sha256:2571ab1e19d9affc28186038b8d74ae1fe7518c74e7c02ec38014f233d9ee339
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2535953895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f587b64bcf621e6c2092e82f495657be303cc62a3e1edf4a6c31f7688be43c6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Wed, 12 Mar 2025 18:49:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:49:55 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Wed, 12 Mar 2025 18:50:57 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_windows_hotspot_21.0.6_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_windows_hotspot_21.0.6_7.msi ;     Write-Host ('Verifying sha256 (c361f8a018cffdad1ad0a0ce3e5032fc7314dec3f73642dc626a6121d487008b) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'c361f8a018cffdad1ad0a0ce3e5032fc7314dec3f73642dc626a6121d487008b') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Mar 2025 18:51:07 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:51:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848830e95a1cac4cad2dc230c851ec2ea7b52a324fa3315593cca23f35a4b33c`  
		Last Modified: Wed, 12 Mar 2025 18:51:10 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e2cc874d304581e58bbaf9023d97740683991756da6d622ba0d604859106b0`  
		Last Modified: Wed, 12 Mar 2025 18:51:10 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729bdb5087904cee94ecb498e47631213506c0dce8271f0836889c7a43118607`  
		Last Modified: Wed, 12 Mar 2025 18:51:28 GMT  
		Size: 380.3 MB (380256920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ef9c8d0ca79461c388eb4a25191fd5f7f9af0cebdec7e8b427e8ca110d4416`  
		Last Modified: Wed, 12 Mar 2025 18:51:11 GMT  
		Size: 4.1 MB (4058437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bdfdb3114790589d93af56626ebe3c3a3d1cf09e87903810012af65ff41efa6`  
		Last Modified: Wed, 12 Mar 2025 18:51:10 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
