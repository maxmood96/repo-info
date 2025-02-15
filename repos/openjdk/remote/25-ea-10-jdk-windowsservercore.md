## `openjdk:25-ea-10-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:28767aa28fa6ac5e29b772233ce9319398d32c776f37f23b262ffbcf3b95aa4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `openjdk:25-ea-10-jdk-windowsservercore` - windows version 10.0.26100.2894; amd64

```console
$ docker pull openjdk@sha256:c30a31eb51414063a3fb71ff138ffa8512ecb9c22bb515e36779d648f262b20c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2709000556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65afc8e5af227114cab13a4e5e4c691344fb47056373dc54a6cbcfd3c40a2c51`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Fri, 14 Feb 2025 23:32:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Feb 2025 23:33:00 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 14 Feb 2025 23:33:01 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 14 Feb 2025 23:33:07 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 14 Feb 2025 23:33:07 GMT
ENV JAVA_VERSION=25-ea+10
# Fri, 14 Feb 2025 23:33:08 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/10/GPL/openjdk-25-ea+10_windows-x64_bin.zip
# Fri, 14 Feb 2025 23:33:08 GMT
ENV JAVA_SHA256=9e8ebedd95dce7d5755f885b28067679019d529df9ff91b64e03edd7f2285e6e
# Fri, 14 Feb 2025 23:33:25 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 14 Feb 2025 23:33:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Wed, 22 Jan 2025 06:04:03 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:630380736f07612a35719b61be2f0d4410c719defdfdf66326453933569f1456`  
		Last Modified: Sat, 15 Feb 2025 00:31:34 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b127f29d47d1334b45d3294161a389e791436052cbb1d5484e70980d6a23069`  
		Last Modified: Sat, 15 Feb 2025 00:31:35 GMT  
		Size: 384.9 KB (384875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6899a068a803177d37a7ed0dce5b252eca438ff80a6939a1779350c367a6d400`  
		Last Modified: Sat, 15 Feb 2025 00:31:35 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e8dd64f9c6078a3f54ab7cc9fd42c63fd8c36f9f4fa8f66e03846cd836bf28e`  
		Last Modified: Sat, 15 Feb 2025 00:31:36 GMT  
		Size: 373.7 KB (373671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f82156f108d2eba6f3fc73bab750e13fdb781d4bbb99ff5b5e90a4fe7b0812ba`  
		Last Modified: Sat, 15 Feb 2025 00:31:37 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f6a1617d806f743adb4b0632a444418953c3b3a69c81aa55404e2902a3ba6a`  
		Last Modified: Sat, 15 Feb 2025 00:31:38 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be161ae7be15305731e6c5422ea7cfa28624c73a110830ed8a1bdfa1aafcf279`  
		Last Modified: Sat, 15 Feb 2025 00:31:38 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f3e00a0056f2cd5de9947f0dc389bedd030d0567397ba870566fec5cf4892b`  
		Last Modified: Sat, 15 Feb 2025 00:31:53 GMT  
		Size: 208.0 MB (207956604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a41399944e676da820aa319e71f292d2980c3c40c6674c50852734dd5fd9f40`  
		Last Modified: Sat, 15 Feb 2025 00:31:43 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-10-jdk-windowsservercore` - windows version 10.0.20348.3207; amd64

```console
$ docker pull openjdk@sha256:4ca9c577bf52ef8ca0ad75ea860b1d36ea3754861f8ffc69426f6f1fded7a57a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2472498047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12c8680638fe9803415a87e3499ea972c048a551111d1e96c0bb7ff41939e899`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Fri, 14 Feb 2025 23:39:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Feb 2025 23:40:07 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 14 Feb 2025 23:40:08 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 14 Feb 2025 23:40:13 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 14 Feb 2025 23:40:14 GMT
ENV JAVA_VERSION=25-ea+10
# Fri, 14 Feb 2025 23:40:14 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/10/GPL/openjdk-25-ea+10_windows-x64_bin.zip
# Fri, 14 Feb 2025 23:40:15 GMT
ENV JAVA_SHA256=9e8ebedd95dce7d5755f885b28067679019d529df9ff91b64e03edd7f2285e6e
# Fri, 14 Feb 2025 23:40:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 14 Feb 2025 23:40:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Wed, 12 Feb 2025 22:14:21 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c93a3bf8cd2242f249b9d733c58358a5b351c5b85efa57992b9bbcb95d7e7e22`  
		Last Modified: Sat, 15 Feb 2025 00:31:21 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d677d07e6535bdd462b3111fb93e10d127c25d8eb264e844d1d0504b1840d30b`  
		Last Modified: Sat, 15 Feb 2025 00:31:22 GMT  
		Size: 367.5 KB (367537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dfc6b0371ba54d8a4975968029d4f9de40ecdf7e329f7f28b4af9c754b48d69`  
		Last Modified: Sat, 15 Feb 2025 00:31:22 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1188cc72becce0dd453532efa5c9dfcc814a45cf438caf467ab7d20e3d9c29fb`  
		Last Modified: Sat, 15 Feb 2025 00:31:23 GMT  
		Size: 346.3 KB (346259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b473e2d8c219e1dae4a4b8cfe77b02440b209ea878076b1ef27387c6aed0ec`  
		Last Modified: Sat, 15 Feb 2025 00:31:23 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96af92c564769b2ff3ce42265a67092268b30f47078b8a294763cffd90f562d1`  
		Last Modified: Sat, 15 Feb 2025 00:31:24 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc9f06e49b9bff0f037f585d9d12b7f7110975dd65ce9104a12770c151db7f53`  
		Last Modified: Sat, 15 Feb 2025 00:31:23 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8881d96f1a722b9a5a82f271c13a3c08003feb3a669c8532a44fb456bc8333`  
		Last Modified: Sat, 15 Feb 2025 00:31:37 GMT  
		Size: 207.9 MB (207918460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a72d415781220633aa7fe1d390139005b37b6d426bd0b9075283fe53fa6518`  
		Last Modified: Sat, 15 Feb 2025 00:31:24 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-10-jdk-windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull openjdk@sha256:e2306fb6bbe0044d1981653843f20607aaa20d5e7c934f30e3b6e8c79227cb5c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2345514662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d9b1be90c4fa9eaefe6e9f4b6dcaaf0ac041edb2d52d2b8ab95342cf0ef6a47`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Fri, 14 Feb 2025 23:36:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Feb 2025 23:37:06 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 14 Feb 2025 23:37:07 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 14 Feb 2025 23:37:12 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 14 Feb 2025 23:37:13 GMT
ENV JAVA_VERSION=25-ea+10
# Fri, 14 Feb 2025 23:37:13 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/10/GPL/openjdk-25-ea+10_windows-x64_bin.zip
# Fri, 14 Feb 2025 23:37:14 GMT
ENV JAVA_SHA256=9e8ebedd95dce7d5755f885b28067679019d529df9ff91b64e03edd7f2285e6e
# Fri, 14 Feb 2025 23:37:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 14 Feb 2025 23:37:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 22:29:28 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a5f72500d7c71b459f7065fe476e845b111c9298cf4b639eb8ec189cd1ef49`  
		Last Modified: Sat, 15 Feb 2025 00:31:24 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7a4f53b9bd006c77e9e5e23e120a305ff9549d0888b82f0bfede2a79ad73d9`  
		Last Modified: Sat, 15 Feb 2025 00:31:24 GMT  
		Size: 351.6 KB (351632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373358639f2bd6d60572f1385106ab9bebfbdd5096a805f8844b781d18d864b9`  
		Last Modified: Sat, 15 Feb 2025 00:31:24 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0127c9a799e6d8dcf09d809a4714edffa952a96821f24983178355c098dff4f8`  
		Last Modified: Sat, 15 Feb 2025 00:31:24 GMT  
		Size: 333.5 KB (333463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8015adf261b47bbdb4e75f539e5be0dfb802a91374adef7a8db08ae6485f998`  
		Last Modified: Sat, 15 Feb 2025 00:31:24 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa4d70cfae89156c91034d5169461cfd4bf2c79d874717e53dd23773bef9480`  
		Last Modified: Sat, 15 Feb 2025 00:31:24 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2aa9fa6b4cbe722ac3bc8fe13973967875d065868f661662c56539169bad07`  
		Last Modified: Sat, 15 Feb 2025 00:31:24 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c651ee7fa4380c117e447bcd5d5502aae2ffe16da48b723294da3156869952a1`  
		Last Modified: Sat, 15 Feb 2025 00:31:41 GMT  
		Size: 207.9 MB (207912975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed9f6e7131e1bdeef944b1f6b31026be94452bf494b1a8b9fcc65df6e71127f`  
		Last Modified: Sat, 15 Feb 2025 00:31:25 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
