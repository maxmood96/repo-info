## `openjdk:25-ea-18-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:05fd1122ee9e5c48024b98826af7c5653346880dab582c1d2a3f96cf3c49bbd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3775; amd64
	-	windows version 10.0.20348.3453; amd64
	-	windows version 10.0.17763.7136; amd64

### `openjdk:25-ea-18-jdk-windowsservercore` - windows version 10.0.26100.3775; amd64

```console
$ docker pull openjdk@sha256:77f162bda00e724a0d2525a72c6707c514ec1ff879cc438662b6f4fd501ca067
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3603479545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee748757f7208a2dadbc267357d82fc6bf020371d35b9c85cfffab3a23c1d11b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 06 Apr 2025 07:48:58 GMT
RUN Install update 10.0.26100.3775
# Mon, 14 Apr 2025 23:05:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 14 Apr 2025 23:05:22 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 14 Apr 2025 23:05:23 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 14 Apr 2025 23:05:31 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 14 Apr 2025 23:05:33 GMT
ENV JAVA_VERSION=25-ea+18
# Mon, 14 Apr 2025 23:05:35 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/18/GPL/openjdk-25-ea+18_windows-x64_bin.zip
# Mon, 14 Apr 2025 23:05:37 GMT
ENV JAVA_SHA256=41f24482b5d173e5a8f242d81909835bd7e85fdb131b901bff9a150186c3c03c
# Mon, 14 Apr 2025 23:05:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 14 Apr 2025 23:05:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761846874dadc4dd9490d5635a266306989ac061986d0e4bcfe36a76ef6888b8`  
		Last Modified: Tue, 08 Apr 2025 21:29:58 GMT  
		Size: 1.2 GB (1179372285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59547f15d816541b9e52f79da41e5915341f9161ea4407c06790e8f499d801e6`  
		Last Modified: Mon, 14 Apr 2025 23:06:05 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2052da3b70068b8084d54a8cc947ba9d64c214dc8af5c47621341dcab19f6fae`  
		Last Modified: Mon, 14 Apr 2025 23:06:05 GMT  
		Size: 409.9 KB (409911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26a2027742f2fb8b2b88d4c10ae07d814c258c0e8fe4cc2cd860bab11f4efc29`  
		Last Modified: Mon, 14 Apr 2025 23:06:05 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24012a31c58ece28351ee6560c6e49a900ee1dc8fdb0d62d065892eb8cb1ba1b`  
		Last Modified: Mon, 14 Apr 2025 23:06:05 GMT  
		Size: 388.0 KB (388039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c996547c40ebafa0f8cd758453bb89e959cddf9ab37fd47c2ca5d27becce4c`  
		Last Modified: Mon, 14 Apr 2025 23:06:03 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a70be02496f600d630ce63232129d27b16ca988c5f72590f75ae5d3ea257c16`  
		Last Modified: Mon, 14 Apr 2025 23:06:03 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1120fbf6386950eebcbd7e341e0e84cc56917a6a7a2b0556f2fc1ce7c6e6dc1`  
		Last Modified: Mon, 14 Apr 2025 23:06:03 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4845737e64f189008c0cba13b849a661c127131aa7374fd1d524a41ab676a57`  
		Last Modified: Mon, 14 Apr 2025 23:06:16 GMT  
		Size: 208.0 MB (207994250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba50aa4cdb293648d84e79b4dee88834c018912b9f24d45eeb1a6d66588777a8`  
		Last Modified: Mon, 14 Apr 2025 23:06:03 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-18-jdk-windowsservercore` - windows version 10.0.20348.3453; amd64

```console
$ docker pull openjdk@sha256:a8cbe5a83fd2c8a7bffb59b4c545c7b7d162a95deaa055da837fabdbdd45b597
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2479666258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa9f08faaef7f0fa1eb27155a7e25f489113adbe436d81f570103b837a098ed9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 04 Apr 2025 23:10:04 GMT
RUN Install update 10.0.20348.3453
# Mon, 14 Apr 2025 23:03:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 14 Apr 2025 23:03:25 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 14 Apr 2025 23:03:26 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 14 Apr 2025 23:03:32 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 14 Apr 2025 23:03:33 GMT
ENV JAVA_VERSION=25-ea+18
# Mon, 14 Apr 2025 23:03:33 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/18/GPL/openjdk-25-ea+18_windows-x64_bin.zip
# Mon, 14 Apr 2025 23:03:34 GMT
ENV JAVA_SHA256=41f24482b5d173e5a8f242d81909835bd7e85fdb131b901bff9a150186c3c03c
# Mon, 14 Apr 2025 23:03:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 14 Apr 2025 23:03:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510f1abe0ffe1466f946291b3ac20345b4a5e2063a896736990eae81bbf4bdb4`  
		Last Modified: Tue, 08 Apr 2025 21:40:38 GMT  
		Size: 808.8 MB (808803243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144f12c177739096ac6703a44526030560394b9864781248bef35f91d8ee1f12`  
		Last Modified: Mon, 14 Apr 2025 23:04:02 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a1eca3f316080aac6c64cb8ada843b52617a71b7ded70271deaf5ac13dfc21`  
		Last Modified: Mon, 14 Apr 2025 23:04:03 GMT  
		Size: 358.9 KB (358855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84edcf4155c652365e893cc33ec447bfe4d527351ee0c671a6e335f7305f9992`  
		Last Modified: Mon, 14 Apr 2025 23:04:02 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a7b8fcfb4d81cc41cc0ff633ccef1f341147312d248d78ea8dc83af65aab936`  
		Last Modified: Mon, 14 Apr 2025 23:04:02 GMT  
		Size: 346.7 KB (346689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:557ac4c52496258109a462055bb88ff225efad1f3fc4041fa1a77538f7ef9930`  
		Last Modified: Mon, 14 Apr 2025 23:04:00 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d992152ae40e2fb0a1914b06ca07b9ab2b90a20640266e20aa9f255265de0dcc`  
		Last Modified: Mon, 14 Apr 2025 23:04:00 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a91c4ee81a97e60912dc2229b0693227f98a6a22d54e0cfcbe9efba703ec846`  
		Last Modified: Mon, 14 Apr 2025 23:04:00 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afbaa182ef67c0eb539b55a36022b49c01f8c843959c19c2bcd1f4146e53e33a`  
		Last Modified: Mon, 14 Apr 2025 23:04:12 GMT  
		Size: 208.0 MB (207957255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e236b022a026ae874b9b8f92aff1d41cdc662e752d12f6ce06659390e896adb`  
		Last Modified: Mon, 14 Apr 2025 23:04:00 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-18-jdk-windowsservercore` - windows version 10.0.17763.7136; amd64

```console
$ docker pull openjdk@sha256:82b9115d9ce19bac431f29d461d9cf41366b7eae62c5dca30f149e0693bc59be
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2371376094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd68f374460b19e7d00f97eafe7ff3db49beabbefa4f1196fcd4fbb36235443`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Mon, 14 Apr 2025 23:01:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 14 Apr 2025 23:01:58 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 14 Apr 2025 23:01:59 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 14 Apr 2025 23:02:06 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 14 Apr 2025 23:02:06 GMT
ENV JAVA_VERSION=25-ea+18
# Mon, 14 Apr 2025 23:02:07 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/18/GPL/openjdk-25-ea+18_windows-x64_bin.zip
# Mon, 14 Apr 2025 23:02:08 GMT
ENV JAVA_SHA256=41f24482b5d173e5a8f242d81909835bd7e85fdb131b901bff9a150186c3c03c
# Mon, 14 Apr 2025 23:02:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 14 Apr 2025 23:02:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901c4f6499be32d72d03acd1b077f303c36f9e02549df1e19e93e6f970009e2e`  
		Last Modified: Mon, 14 Apr 2025 23:02:37 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6b8435c9a9649b98ba88785e7bf6465520b54419856cf1fc5db334b067d2ad`  
		Last Modified: Mon, 14 Apr 2025 23:02:37 GMT  
		Size: 341.7 KB (341685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:842b230d555934e825a14324149c16f66c7014b6e8bb7651a898041ee671e45d`  
		Last Modified: Mon, 14 Apr 2025 23:02:37 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f43866e1dcafdf28f4228409e7ba028feb8636b24ff7f354045ae263091c14`  
		Last Modified: Mon, 14 Apr 2025 23:02:37 GMT  
		Size: 333.1 KB (333086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1ccac9761890f7f40a1d1f6dff046a49acef0e861085317fcedff81f3bfd42`  
		Last Modified: Mon, 14 Apr 2025 23:02:35 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:728d117ea3c13782050bb4a5f47e6dd5262c2b8ac6fed617a386a78ebf37b227`  
		Last Modified: Mon, 14 Apr 2025 23:02:35 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f101e1391c24c0c7c48aae7c9ad7c7041f39b242c99fe1ea34338ff5647e557`  
		Last Modified: Mon, 14 Apr 2025 23:02:35 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7704872e5346a4a65f26e58a263307eab434bc65fe32064a6461f9bbc161cf3d`  
		Last Modified: Mon, 14 Apr 2025 23:02:46 GMT  
		Size: 208.0 MB (207967651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd85a721ad333995528bd0b2888dbac19cbf4830018f77b6f2d724f226a5b2c5`  
		Last Modified: Mon, 14 Apr 2025 23:02:35 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
