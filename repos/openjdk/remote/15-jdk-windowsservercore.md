## `openjdk:15-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:12d80b2e3c9fc4081f28cc0e65105f7f487549ee59364780f4619b435fefd800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64
	-	windows version 10.0.14393.3686; amd64

### `openjdk:15-jdk-windowsservercore` - windows version 10.0.17763.1217; amd64

```console
$ docker pull openjdk@sha256:8811f85dbf4eab286f98cf9aaa7162c7fc121f16132bddec6ae83d794eb28690
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1910616193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089852659bbb1e5e87e70fe0e92328592b0bd9b7826a3fdc9c16d702b329981b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 12:41:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 May 2020 15:22:51 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Wed, 13 May 2020 15:22:52 GMT
ENV JAVA_HOME=C:\openjdk-15
# Wed, 13 May 2020 15:23:14 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Sat, 23 May 2020 01:15:24 GMT
ENV JAVA_VERSION=15-ea+24
# Sat, 23 May 2020 01:15:25 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/24/GPL/openjdk-15-ea+24_windows-x64_bin.zip
# Sat, 23 May 2020 01:15:26 GMT
ENV JAVA_SHA256=058abe6c027572c237434b8a82d12b07cff7b4a304b7d784b1da73a48393e135
# Sat, 23 May 2020 01:17:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 23 May 2020 01:17:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:77613e754ba9d62c0acd4ef271c4ee7d3af091b8c8b310afa404560a9d281f82`  
		Last Modified: Wed, 13 May 2020 13:00:20 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc1950cbc28db7632bd0afe94e7afdd5ca08b3a3ca57687e6a837312b287f7a`  
		Last Modified: Wed, 13 May 2020 16:04:15 GMT  
		Size: 347.0 KB (346988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccd9bd22f75be58d6e2a85f96e44ed57e761dd5917328d2ab7a827a81241f7e`  
		Last Modified: Wed, 13 May 2020 16:04:15 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928fd42a12a95b96ecfd3687faac5e7c17ace93c556f6920de761fb801902ada`  
		Last Modified: Wed, 13 May 2020 16:04:15 GMT  
		Size: 300.4 KB (300354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8675da8bad90838dbf1590728f262479c0ed7e94e5ecc19e625e7ca394964ca2`  
		Last Modified: Sat, 23 May 2020 01:25:30 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c27c441b96e16ae6c0ee76ce550c27432f50e2493435f97fe88fd5b154708ea`  
		Last Modified: Sat, 23 May 2020 01:25:30 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2888406cec9eb7d8f64f0be960c854b3d2aa5ef88f0e5751623131d7048cdca9`  
		Last Modified: Sat, 23 May 2020 01:25:29 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0efb2fc710393c323fad889320eebd0a2cea59fdbe4187563998794cdda9cd3`  
		Last Modified: Sat, 23 May 2020 01:25:52 GMT  
		Size: 191.6 MB (191629111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53dbde430dff6853830d6333223e2247da6713d8f009f09fd0b2725b435c80ef`  
		Last Modified: Sat, 23 May 2020 01:25:29 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:15-jdk-windowsservercore` - windows version 10.0.14393.3686; amd64

```console
$ docker pull openjdk@sha256:476c66abcf4d197ded8f87f3ab82b893ed87f16558ad8f0765fc17628395efdd
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5939294032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c59defecd4bb9f053f85d21e2c0337494011b6150eb87000bc106d13ffbb7d36`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 12:34:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 May 2020 15:26:34 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Wed, 13 May 2020 15:26:35 GMT
ENV JAVA_HOME=C:\openjdk-15
# Wed, 13 May 2020 15:27:52 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Sat, 23 May 2020 01:17:35 GMT
ENV JAVA_VERSION=15-ea+24
# Sat, 23 May 2020 01:17:36 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/24/GPL/openjdk-15-ea+24_windows-x64_bin.zip
# Sat, 23 May 2020 01:17:37 GMT
ENV JAVA_SHA256=058abe6c027572c237434b8a82d12b07cff7b4a304b7d784b1da73a48393e135
# Sat, 23 May 2020 01:20:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 23 May 2020 01:20:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b940e70a4619b357d89f3dcabf4ac263d1efc65e1ef3af64cb0e8fbeaccc64dd`  
		Size: 1.7 GB (1661903967 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e3e9730c43354781e87aa51e853bff3b1e8c1ca7004f527139638a8f9d499c49`  
		Last Modified: Wed, 13 May 2020 12:59:27 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a56eaed4a20d0f67d3d00bc23ac486a70424c1d5ebc2b77f4b3bf17c8fcf765d`  
		Last Modified: Wed, 13 May 2020 16:08:25 GMT  
		Size: 5.4 MB (5382606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19edd7328d1003d3b7eb7cc52937a9ad37740aeddce56a7db9cf0cbff77e015`  
		Last Modified: Wed, 13 May 2020 16:08:23 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78316c2a5c012f8c77766fd738f4887044ffc57b19cc57ce29a90b94edbef075`  
		Last Modified: Wed, 13 May 2020 16:08:28 GMT  
		Size: 5.4 MB (5362683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd77ef67b1f899df7c46013c651ff91d89cde0ab1c40c8e8cb6c5ded5e97838`  
		Last Modified: Sat, 23 May 2020 01:26:17 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba464519853437c28cf282916a757ca51bd186e9b96b1e01f3515d084a9830f3`  
		Last Modified: Sat, 23 May 2020 01:26:17 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9776da0d9494eb97bdb729d5b203e032ae9ef719eb20d09fb666b27183ec189`  
		Last Modified: Sat, 23 May 2020 01:26:17 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e6eb85f83d3e34da7120a46478db469fc9bf1d340f07e7dedeabf65d43ae77`  
		Last Modified: Sat, 23 May 2020 01:26:44 GMT  
		Size: 196.7 MB (196651976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b6e7f2e0a989522abd8a15bcc9307ab31eb99e4652624433880d250a0b913c`  
		Last Modified: Sat, 23 May 2020 01:26:17 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
