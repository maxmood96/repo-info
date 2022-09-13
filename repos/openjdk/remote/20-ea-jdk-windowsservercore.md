## `openjdk:20-ea-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:5354b3915c5b3b766bec59e4a6b9a12d8ffc2b8820d0cfcb95d72c9d12c2a922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.887; amd64
	-	windows version 10.0.17763.3287; amd64

### `openjdk:20-ea-jdk-windowsservercore` - windows version 10.0.20348.887; amd64

```console
$ docker pull openjdk@sha256:18ffd36bdac05c63225d1b661e13c3d0dafeebd4c2cfbc9d326dbc197326f1e9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2510485232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf15fbe6b22db9bcf8d7034c372c414c37a1a2d96749a1d602dbf7b5f8df823e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Sat, 06 Aug 2022 02:59:35 GMT
RUN Install update 10.0.20348.887
# Wed, 10 Aug 2022 12:11:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Aug 2022 16:55:00 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 10 Aug 2022 16:55:00 GMT
ENV JAVA_HOME=C:\openjdk-20
# Wed, 10 Aug 2022 16:55:20 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 12 Sep 2022 22:26:31 GMT
ENV JAVA_VERSION=20-ea+14
# Mon, 12 Sep 2022 22:26:32 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk20/14/GPL/openjdk-20-ea+14_windows-x64_bin.zip
# Mon, 12 Sep 2022 22:26:33 GMT
ENV JAVA_SHA256=9a074e380bbef6c389a660f1f21bf1cfc449cee8d6c387f4422305b2feb06dc5
# Mon, 12 Sep 2022 22:27:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 12 Sep 2022 22:27:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:97b25a378238b615dc51216c4d87ce17fd3cc3dca9db458e8705d1a4c17e3bb7`  
		Size: 880.0 MB (880025531 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4a5e3787c778295a5877e0381020b02273a985f7db2dd483ddff586869546e4c`  
		Last Modified: Wed, 10 Aug 2022 12:42:34 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0cc935c154780815cf1fb6065aa1c262b52a7648b984b06133beb4e95833c0`  
		Last Modified: Wed, 10 Aug 2022 17:27:08 GMT  
		Size: 624.7 KB (624700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43525a703370320083aa7f64beeb4176b2090f555b73f9be7f9cb9fbda9f5736`  
		Last Modified: Wed, 10 Aug 2022 17:27:07 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf27aca426cd52616bfeb5296c1b75f2095211cf6c91d27a306c654522f65a32`  
		Last Modified: Wed, 10 Aug 2022 17:27:08 GMT  
		Size: 557.0 KB (557029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183ea27befb7b75a74b9cab96551b9bbfa0c7751df06a28fa42efbd05560a830`  
		Last Modified: Mon, 12 Sep 2022 22:32:13 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e3b935728d4fab1d3274f8f9f9ad5e299cd255c20b18d21646c3297741910be`  
		Last Modified: Mon, 12 Sep 2022 22:32:13 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b090efe8a6615c7523c30534cad5f24fb8d40f19aaf14f886bfccc47bdad8abc`  
		Last Modified: Mon, 12 Sep 2022 22:32:13 GMT  
		Size: 1.4 KB (1450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309b2ec559b86f6e4ec701c1e8429e31760fe4eed154f70fe95c7fc23f55f6e2`  
		Last Modified: Mon, 12 Sep 2022 22:32:33 GMT  
		Size: 192.4 MB (192405855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9746075a53ad1a28f5bbc17fd035f666b65380e362af8691b89cb366f11de290`  
		Last Modified: Mon, 12 Sep 2022 22:32:13 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-jdk-windowsservercore` - windows version 10.0.17763.3287; amd64

```console
$ docker pull openjdk@sha256:e502335749d7ebf80b181ca1312d543a4ddb471116d3ade2bb7f4e77b9f259a2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2870551553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59463ea747324e7279fbb51eda8c53a7a7b0931b1d8dd5aa2a57982dc90f619e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 06 Aug 2022 18:30:32 GMT
RUN Install update 10.0.17763.3287
# Wed, 10 Aug 2022 12:16:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Aug 2022 16:57:20 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 10 Aug 2022 16:57:21 GMT
ENV JAVA_HOME=C:\openjdk-20
# Wed, 10 Aug 2022 16:58:18 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 12 Sep 2022 22:27:34 GMT
ENV JAVA_VERSION=20-ea+14
# Mon, 12 Sep 2022 22:27:35 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk20/14/GPL/openjdk-20-ea+14_windows-x64_bin.zip
# Mon, 12 Sep 2022 22:27:36 GMT
ENV JAVA_SHA256=9a074e380bbef6c389a660f1f21bf1cfc449cee8d6c387f4422305b2feb06dc5
# Mon, 12 Sep 2022 22:29:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 12 Sep 2022 22:29:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:294d77ac553d7210b662d07674ef9e39a6c2e88dc15b9d2788d51e509bc8b54e`  
		Size: 800.5 MB (800546641 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d64f32398ff5e4ac4cbab317ffed87a2fbf4e4a37210284dba19f2929d631a95`  
		Last Modified: Wed, 10 Aug 2022 12:42:57 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9df80b59d75310c5b623001e9a6fefa8c2f0255dfbb8c58e60daa3aba0f9c6`  
		Last Modified: Wed, 10 Aug 2022 17:27:52 GMT  
		Size: 347.3 KB (347323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a313f85e8b9975fcba0bc4920f5caf6d1aca17b778349b49c87d1633e7ae60eb`  
		Last Modified: Wed, 10 Aug 2022 17:27:51 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448a04775e0e1c17f4166d28a03de82719ce659ec910523df8a06c97c94a7d3b`  
		Last Modified: Wed, 10 Aug 2022 17:27:51 GMT  
		Size: 309.6 KB (309626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58a3582f5838510c85efe40e90ef6e0a0890d9c685ff786f61799654d97ba79`  
		Last Modified: Mon, 12 Sep 2022 22:32:52 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:766bf755100956560165dad42adfeb275f94a466263c34e6a122d70f20e71e21`  
		Last Modified: Mon, 12 Sep 2022 22:32:52 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7417de3c3175f194b54af1ff3a89a84ca3b9d1bc74814fe3f7d80a4f05981f`  
		Last Modified: Mon, 12 Sep 2022 22:32:52 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bdcd300930c830b6338e93212d108b0b11e93d67e4f16b688a77862c45d534e`  
		Last Modified: Mon, 12 Sep 2022 22:33:12 GMT  
		Size: 192.2 MB (192173410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a9c67810b08f37768ae32a6753e786f33674d9758836469118fdb9f436469c0`  
		Last Modified: Mon, 12 Sep 2022 22:32:52 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
