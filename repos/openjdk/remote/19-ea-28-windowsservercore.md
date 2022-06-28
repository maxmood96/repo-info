## `openjdk:19-ea-28-windowsservercore`

```console
$ docker pull openjdk@sha256:b0ad9dbfaef88091fbc3a5ee2de5c5668772fe46008d4b9651aac86d1c211283
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.768; amd64
	-	windows version 10.0.17763.3046; amd64

### `openjdk:19-ea-28-windowsservercore` - windows version 10.0.20348.768; amd64

```console
$ docker pull openjdk@sha256:14823412b71e469b38f69ad9063838f0441ad31fa702af6cde23c49961c27e39
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2471426877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca49703cf399cbcb7f77fb1930dc5a067a42bf3f6dfd7c03b8cb06d3ac81cfab`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 09 Jun 2022 04:32:50 GMT
RUN Install update 10.0.20348.768
# Wed, 15 Jun 2022 12:13:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jun 2022 19:30:14 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 15 Jun 2022 19:30:15 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 15 Jun 2022 19:30:37 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 28 Jun 2022 00:19:12 GMT
ENV JAVA_VERSION=19-ea+28
# Tue, 28 Jun 2022 00:19:13 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk19/28/GPL/openjdk-19-ea+28_windows-x64_bin.zip
# Tue, 28 Jun 2022 00:19:15 GMT
ENV JAVA_SHA256=fea53e784593c7b5b9da4bdfc7deaa8957864ccc302faf224c45c3e1be7156dc
# Tue, 28 Jun 2022 00:20:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 28 Jun 2022 00:20:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6c71967ff41928927e4c407171e4ffbac3c9ab4221eb64f5ca5a34ff4c230567`  
		Size: 841.6 MB (841600427 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dec0338feaf01f35eb916b7fd9ecc08b719354163254885d5215e513c1a3eb2e`  
		Last Modified: Wed, 15 Jun 2022 12:49:26 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b6e059d50cccbff94037bf242f1b94acf1cc939d701dff58c07f4fcfdc9767`  
		Last Modified: Wed, 15 Jun 2022 20:02:04 GMT  
		Size: 632.3 KB (632288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4256811745995e57de7802acfc5bdccb9f2755ed41ecb3647d39dc12e6561352`  
		Last Modified: Wed, 15 Jun 2022 20:02:04 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83c911f706211694bdb53a7b8921b9b41f12cd4a52237dfdc7d74f3cc8585a5b`  
		Last Modified: Wed, 15 Jun 2022 20:02:04 GMT  
		Size: 562.5 KB (562533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:023b5def5fec32fb0fb48cf031244acb15de75e70b46b8bbcc10f1059567d810`  
		Last Modified: Tue, 28 Jun 2022 02:25:43 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636a4ce1ccf354cea77de8b7512bb8aa60a4eec7103fb00d9942f95e35694d24`  
		Last Modified: Tue, 28 Jun 2022 02:25:43 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff75da5072a5ed728d3fc19f0aadf8a38406ca2f824777be0cb9c738d439b91c`  
		Last Modified: Tue, 28 Jun 2022 02:25:43 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0fd82fc80744bf75221b5ee6feef8626405cc7b4e9d5201d4a70a2a78b9da8f`  
		Last Modified: Tue, 28 Jun 2022 02:29:14 GMT  
		Size: 191.8 MB (191759543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeccfc1cab4fa75a787c088eeece53831d5c05297f4e996b9237c24b567a7dfc`  
		Last Modified: Tue, 28 Jun 2022 02:25:43 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-ea-28-windowsservercore` - windows version 10.0.17763.3046; amd64

```console
$ docker pull openjdk@sha256:10a0209685877cb530f6a22de49e1d877d76cfeb68d96e96e46e27bd1211cebd
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2855481585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b279933229196a8365c107bc5c718d085fd44bc990c2c95c1a3a282ffbc5ae7`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 09 Jun 2022 19:41:03 GMT
RUN Install update 10.0.17763.3046
# Wed, 15 Jun 2022 12:18:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jun 2022 19:33:08 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 15 Jun 2022 19:33:09 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 15 Jun 2022 19:34:17 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 28 Jun 2022 00:20:25 GMT
ENV JAVA_VERSION=19-ea+28
# Tue, 28 Jun 2022 00:20:26 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk19/28/GPL/openjdk-19-ea+28_windows-x64_bin.zip
# Tue, 28 Jun 2022 00:20:27 GMT
ENV JAVA_SHA256=fea53e784593c7b5b9da4bdfc7deaa8957864ccc302faf224c45c3e1be7156dc
# Tue, 28 Jun 2022 00:21:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 28 Jun 2022 00:21:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc6ae6c5aa2b4920ae68469c5e7e7c3a3c85e5eaafc24660e7b3adb21d6fce77`  
		Size: 786.1 MB (786113785 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4ed911f97ae3a2a6279c70738e5692b14369ac11871a2bbd2f6ad301419527ad`  
		Last Modified: Wed, 15 Jun 2022 12:50:13 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75415e053743ebceabbf30d0a8101d97dd712c88fc012c45f1df824cbac48e21`  
		Last Modified: Wed, 15 Jun 2022 20:05:58 GMT  
		Size: 354.4 KB (354400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7116bbe0a121cf02a096d9baf075b263a14bef9d19f19247ba9301ce1510d4d3`  
		Last Modified: Wed, 15 Jun 2022 20:05:58 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859adb7dcc86ae2af5eb7ae3f7bfb7a657d7100c15621b21c36436c2be52ac0c`  
		Last Modified: Wed, 15 Jun 2022 20:05:58 GMT  
		Size: 312.2 KB (312220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b204d6ac5fb8df3ae5f41003c391858e639297d37bfd7632dd4fc3a99a96398f`  
		Last Modified: Tue, 28 Jun 2022 02:29:35 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f08742719233c52e7f2df2ff9ec7f60fbbbc44ef99aed33455d558919d9cde28`  
		Last Modified: Tue, 28 Jun 2022 02:29:35 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4180a9c8835133dca8283f7ecb68b7e441c8e8e825a1e9ba52a4a7528075513`  
		Last Modified: Tue, 28 Jun 2022 02:29:35 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b607a44580d0359ded598cd3e381918fd4faf7567eb23eff5560684e89f30ad9`  
		Last Modified: Tue, 28 Jun 2022 02:33:05 GMT  
		Size: 191.5 MB (191526697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:434e5f97889d133ec4d6209a6dfe57444d11b6ca499dc9a7b3a8bd407835f8c6`  
		Last Modified: Tue, 28 Jun 2022 02:29:35 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
