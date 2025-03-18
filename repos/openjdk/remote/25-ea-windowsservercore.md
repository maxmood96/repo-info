## `openjdk:25-ea-windowsservercore`

```console
$ docker pull openjdk@sha256:4192a1c57bc0b8b996abd7ce18cb6c1f669f25c8fad41ab71ad636f166c18252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `openjdk:25-ea-windowsservercore` - windows version 10.0.26100.3476; amd64

```console
$ docker pull openjdk@sha256:c5144b6ea730ca344a430ae864f9f09e0f27aec3d31f54ea4d8963fab9d2177c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3117318277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4389ff7e2d04125ac8aa3906dc85447d31241edbd5294a77f9d2a9cfbd402d3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Mon, 17 Mar 2025 21:15:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 17 Mar 2025 21:15:31 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 17 Mar 2025 21:15:32 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 17 Mar 2025 21:15:38 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 17 Mar 2025 21:15:39 GMT
ENV JAVA_VERSION=25-ea+14
# Mon, 17 Mar 2025 21:15:39 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/14/GPL/openjdk-25-ea+14_windows-x64_bin.zip
# Mon, 17 Mar 2025 21:15:40 GMT
ENV JAVA_SHA256=4616b55a7c0d6b65d650a08986609158fbffcfed8fc5fa589e9f356898d735d0
# Mon, 17 Mar 2025 21:15:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 17 Mar 2025 21:16:02 GMT
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
	-	`sha256:c5fc1859cd7cbca3bb7a2cbcfd11c1a147b8396d7084f3ed75bd06f0bde8390e`  
		Last Modified: Mon, 17 Mar 2025 21:16:09 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:797f3cdd1cb14a320e37695414677de17b379d87e5fe21ad5a370380825af188`  
		Last Modified: Mon, 17 Mar 2025 21:16:10 GMT  
		Size: 396.2 KB (396165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a56ce755c07a814b5098d4810d5fd2acd6a76f6ad18b287b84e74b751f4ea4f6`  
		Last Modified: Mon, 17 Mar 2025 21:16:09 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9291d5ae2b14f441336980fba5496dd3175fe8b02c4cc1b89d76cd21ac3f0d11`  
		Last Modified: Mon, 17 Mar 2025 21:16:09 GMT  
		Size: 378.8 KB (378775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c53ad5970bcdcc780b072072e7a297cde1ba0375d5624f25be5f9269aa89d5`  
		Last Modified: Mon, 17 Mar 2025 21:16:08 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553c677e4f5901e48b2deba852ce22964898e3d67e586f7e139f31fa3ad35df6`  
		Last Modified: Mon, 17 Mar 2025 21:16:08 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6768ef7fe08d0e2a960f84ad570a08a98e237ef5c16555f1e044d193ca205e66`  
		Last Modified: Mon, 17 Mar 2025 21:16:08 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85f9cc630b55752189667ce14d6b4cfa081544f2be592fa69b7a1c40f555d3fa`  
		Last Modified: Mon, 17 Mar 2025 21:16:21 GMT  
		Size: 207.9 MB (207887798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f780d22cadffda04063ac4f5e4680577d6a7c99c257a8672b61ffc8f1809c628`  
		Last Modified: Mon, 17 Mar 2025 21:16:08 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-windowsservercore` - windows version 10.0.20348.3328; amd64

```console
$ docker pull openjdk@sha256:b3d8bc6fcf844f545a3c6c357a163f344c79a0b36752755ca727ee52a386dfac
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2478503126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af98dd5bcd65ff6b3df99c313f99f9d11423ee674c5514785fc90aa95b24d9bb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Mon, 17 Mar 2025 21:13:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 17 Mar 2025 21:13:59 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 17 Mar 2025 21:14:00 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 17 Mar 2025 21:14:06 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 17 Mar 2025 21:14:07 GMT
ENV JAVA_VERSION=25-ea+14
# Mon, 17 Mar 2025 21:14:08 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/14/GPL/openjdk-25-ea+14_windows-x64_bin.zip
# Mon, 17 Mar 2025 21:14:09 GMT
ENV JAVA_SHA256=4616b55a7c0d6b65d650a08986609158fbffcfed8fc5fa589e9f356898d735d0
# Mon, 17 Mar 2025 21:14:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 17 Mar 2025 21:14:30 GMT
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
	-	`sha256:229e64bcffaf51716797ae399692049522cb84f67c9645a7c49eb08e9f0690af`  
		Last Modified: Mon, 17 Mar 2025 21:14:37 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd431b4b92ee3bc6fc7b4221d7da302fa1f7c272f6c213509ee7d5f3c3db76c0`  
		Last Modified: Mon, 17 Mar 2025 21:14:37 GMT  
		Size: 361.7 KB (361746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae2267affaa0a919f3d988547257009171c212272945d9a5f106a412c447320`  
		Last Modified: Mon, 17 Mar 2025 21:14:37 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51313b10bf56c0615e377a6472ec93e3fd29bf5262fbcf3a3c59fbe1ea0ca722`  
		Last Modified: Mon, 17 Mar 2025 21:14:37 GMT  
		Size: 347.1 KB (347117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25d2f6e130f0b01b3b489e4118a1992efee59c43bfe4420922a3615f19b64da9`  
		Last Modified: Mon, 17 Mar 2025 21:14:35 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31e69fd1411c9ec5de4e92c6fbfcf888b2a3436bd3b544c328578bbdd837cc60`  
		Last Modified: Mon, 17 Mar 2025 21:14:35 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e49083d98971cb7f161b9f38908c16f35a77b7e173165c7b9aa0a2002eab015`  
		Last Modified: Mon, 17 Mar 2025 21:14:35 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a35758e85e8afe57bf9cbdd31829275bb06c4e81eb5b9bae6eafea801bfe27`  
		Last Modified: Mon, 17 Mar 2025 21:14:46 GMT  
		Size: 207.8 MB (207845354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c39cc125df696825f83eef46cd919e92a1764344679f62d1054c6895417ad2`  
		Last Modified: Mon, 17 Mar 2025 21:14:35 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-windowsservercore` - windows version 10.0.17763.7009; amd64

```console
$ docker pull openjdk@sha256:2db8809ea2bd63d825d214e68cd138cf8f335db83e1ba2bb17e71c46b6639abe
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2360153366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3602d7d3a5a48efd4fb7c98f00e56813e7fa1ae00bd3e19b23162df067d60e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Mon, 17 Mar 2025 21:16:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 17 Mar 2025 21:16:58 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 17 Mar 2025 21:16:58 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 17 Mar 2025 21:17:04 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 17 Mar 2025 21:17:05 GMT
ENV JAVA_VERSION=25-ea+14
# Mon, 17 Mar 2025 21:17:05 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/14/GPL/openjdk-25-ea+14_windows-x64_bin.zip
# Mon, 17 Mar 2025 21:17:06 GMT
ENV JAVA_SHA256=4616b55a7c0d6b65d650a08986609158fbffcfed8fc5fa589e9f356898d735d0
# Mon, 17 Mar 2025 21:17:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 17 Mar 2025 21:17:30 GMT
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
	-	`sha256:4b63c86f7839a930dbd1846acfd3ad4b1a64a13f6b576c382b05fd1939375f15`  
		Last Modified: Mon, 17 Mar 2025 21:17:34 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0c80b8e1d84918f51d0dcddc9763d92bd252cfd0fb95b1059b76a115141409`  
		Last Modified: Mon, 17 Mar 2025 21:17:34 GMT  
		Size: 340.6 KB (340643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f68dd6cd9e38825b3d1d90daa7b55cc2802e01d6c6e8a01f399916fadcbbbb38`  
		Last Modified: Mon, 17 Mar 2025 21:17:34 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71af051fd9a3191b2dafedb8742e7e48ccaa574afebc3962c72f765ec74b003b`  
		Last Modified: Mon, 17 Mar 2025 21:17:34 GMT  
		Size: 331.3 KB (331315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245ac7785c6f9900bc46db349c250a68344bc18f8b36903b7461575422d9327b`  
		Last Modified: Mon, 17 Mar 2025 21:17:32 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0769b485ed16adb6e79150c889bd1633c5148fe06257866651a2d92c636a7f1`  
		Last Modified: Mon, 17 Mar 2025 21:17:33 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d9b21ec5a23a3abe941d46a4330382e7f7e0f171ad11222577efd9f6cbcc83`  
		Last Modified: Mon, 17 Mar 2025 21:17:32 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7983c95fae05d038284d0d189b03edb6c7ac0b0cf1e29c3ee5beb1782d4f8b2`  
		Last Modified: Mon, 17 Mar 2025 21:17:45 GMT  
		Size: 207.8 MB (207839003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a725c431b934368e5a5ee950494040a14f945ab97fed4d6e774812b2ff779e5`  
		Last Modified: Mon, 17 Mar 2025 21:17:32 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
