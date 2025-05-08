## `openjdk:25-windowsservercore`

```console
$ docker pull openjdk@sha256:fefff2d3109ba2596a4615201c7ca8f324faf3d2f1ad4f43c86abd593d945391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3781; amd64
	-	windows version 10.0.20348.3566; amd64
	-	windows version 10.0.17763.7249; amd64

### `openjdk:25-windowsservercore` - windows version 10.0.26100.3781; amd64

```console
$ docker pull openjdk@sha256:28ef61f7f012fb42dd9888549ebe132a0013d93868483dbf842231cbd61e5499
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3605190364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5a21ade6abdd5b85963089e0cbf7a7a0964f1956f54ed2ba10b3ed852be6d70`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Tue, 15 Apr 2025 10:03:37 GMT
RUN Install update 10.0.26100.3781
# Mon, 05 May 2025 17:35:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 05 May 2025 17:35:48 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 05 May 2025 17:35:51 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 05 May 2025 17:36:00 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 05 May 2025 17:36:02 GMT
ENV JAVA_VERSION=25-ea+21
# Mon, 05 May 2025 17:36:05 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/21/GPL/openjdk-25-ea+21_windows-x64_bin.zip
# Mon, 05 May 2025 17:36:07 GMT
ENV JAVA_SHA256=50dc1f432a184e23ec8364a00fb4a5f8f791d3eed3a4d36226a041d7de9047e0
# Mon, 05 May 2025 17:36:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 05 May 2025 17:36:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a55b9bd12cfb5d81d64963683e6d5d0ba9423233c85140eff135128a64f7ee`  
		Last Modified: Thu, 08 May 2025 17:36:06 GMT  
		Size: 1.2 GB (1179854238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9dc1da20dd7d9d66beced684a90f4859dade9e83ec2aac06a0cda2f32b90418`  
		Last Modified: Mon, 05 May 2025 17:36:38 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385128f8e202473808c7de73ddbf3661a28dc9281ca8149c262b66aed6e68886`  
		Last Modified: Mon, 05 May 2025 17:36:38 GMT  
		Size: 391.6 KB (391590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:480086c53bfc672e0ee5d52f9f3ff30bbac7761df23f90c90bb598ec3c089f9c`  
		Last Modified: Mon, 05 May 2025 17:36:38 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9460df07f40ad4c56d41deac5cd729ae9ba4a3b75b5e8ba6564d5800c68fa6b0`  
		Last Modified: Mon, 05 May 2025 17:36:38 GMT  
		Size: 374.7 KB (374711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920e99fd7087652f68664fcf6e5e6e03b0b8e080cb8174697bd6111f7b40593e`  
		Last Modified: Mon, 05 May 2025 17:36:36 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37c8169f4efe0081182d1906c41dc6f26ede7dceba957fa5324b0c6c16073e8f`  
		Last Modified: Mon, 05 May 2025 17:36:36 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6562b557d0f6ec04818ed22039d36a565b1df9bdfa6ee808936144715985aaab`  
		Last Modified: Mon, 05 May 2025 17:36:36 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f25f2253c13feacc4b7a68d57791154e5a84c3e8ad367035a719df517e6bf5`  
		Last Modified: Mon, 05 May 2025 17:36:50 GMT  
		Size: 209.3 MB (209254866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d51423187e6601617dfc769b0100176125ff68016f435d4940528a8daead750`  
		Last Modified: Mon, 05 May 2025 17:36:36 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-windowsservercore` - windows version 10.0.20348.3566; amd64

```console
$ docker pull openjdk@sha256:397ca7e38b5b74a81757496212f1c65f26716627eab0d01300acd8a61d39c57f
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2483483728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63829a33fd7840bf71ba4f707ba69e91920a6c1052afa4631c9eabd6cd93d54b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Mon, 05 May 2025 17:29:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 05 May 2025 17:31:03 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 05 May 2025 17:31:04 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 05 May 2025 17:31:17 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 05 May 2025 17:31:18 GMT
ENV JAVA_VERSION=25-ea+21
# Mon, 05 May 2025 17:31:19 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/21/GPL/openjdk-25-ea+21_windows-x64_bin.zip
# Mon, 05 May 2025 17:31:20 GMT
ENV JAVA_SHA256=50dc1f432a184e23ec8364a00fb4a5f8f791d3eed3a4d36226a041d7de9047e0
# Mon, 05 May 2025 17:31:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 05 May 2025 17:31:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6ee194dfee460cc53e0f761b7ff976c08380d6cd1e70cc50ff92cfa99d176`  
		Last Modified: Thu, 08 May 2025 17:22:47 GMT  
		Size: 811.4 MB (811390127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77fe7ba8fcbeae3a54a422b9b8dbf0b9121bb120cf75d491227247c2eb7d58d6`  
		Last Modified: Mon, 05 May 2025 17:31:54 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3b13adf06acb720df564d4777bdda93c0ddb9521686cd8677870f3229c8135`  
		Last Modified: Mon, 05 May 2025 17:31:54 GMT  
		Size: 369.6 KB (369582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0996a0a18f83ff41e65217749193939342b4ea74d255b4a645d15065823a73a`  
		Last Modified: Mon, 05 May 2025 17:31:54 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0924f0a971e566d029767519052116c9c1b3ac4667631b105ce3c12b204a417`  
		Last Modified: Mon, 05 May 2025 17:31:54 GMT  
		Size: 320.7 KB (320679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d26788f68ea4c1ba446d6017ddbc2841a354849cce5f921f582c5ebe8082aebb`  
		Last Modified: Mon, 05 May 2025 17:31:52 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07a9b3d0c7d692bc4ca6b84a3cee100ac2aa34750fcb4cbf3c69fb25cb0b6dc`  
		Last Modified: Mon, 05 May 2025 17:31:52 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e2130f964c70ddd6cb327a0013e1ce68c04bae156f8273d04cbd93b59ee74b`  
		Last Modified: Mon, 05 May 2025 17:31:52 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde7b2a55a26ea1f5f1fa39b4a446354bb74d75e036f4f257a1e691c0f3c66f4`  
		Last Modified: Mon, 05 May 2025 17:32:03 GMT  
		Size: 209.2 MB (209203206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1760b30e3ff436378d8c3d843d51e580027d45e49ccdb3419f611873beed62da`  
		Last Modified: Mon, 05 May 2025 17:31:52 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-windowsservercore` - windows version 10.0.17763.7249; amd64

```console
$ docker pull openjdk@sha256:e66aeb5929210a4e9cddd4e43bd714ed7b68ca3f803b048b45c88e4072001df8
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2375422781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc5435f6646798a88d8e6ca25a9b48ae80d28f6da957ca477cfc77f9f7deae7`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Mon, 05 May 2025 17:30:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 05 May 2025 17:33:44 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 05 May 2025 17:33:45 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 05 May 2025 17:33:58 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 05 May 2025 17:33:58 GMT
ENV JAVA_VERSION=25-ea+21
# Mon, 05 May 2025 17:33:59 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/21/GPL/openjdk-25-ea+21_windows-x64_bin.zip
# Mon, 05 May 2025 17:33:59 GMT
ENV JAVA_SHA256=50dc1f432a184e23ec8364a00fb4a5f8f791d3eed3a4d36226a041d7de9047e0
# Mon, 05 May 2025 17:34:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 05 May 2025 17:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Thu, 08 May 2025 17:14:51 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d33ab57eea3ac259c13042d3b5aa44c76b9bb1d5bcb1c32cbbf392de50d776c`  
		Last Modified: Mon, 05 May 2025 17:34:51 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dbbd0e4b759e40eac1be5bd24a028ae190614dbf3fdad435620c9d5684e0bef`  
		Last Modified: Mon, 05 May 2025 17:34:51 GMT  
		Size: 364.4 KB (364360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9213bbf4fd86b63c038405e6baec91de91f5b6da81bf611f3ce1e1eb0fafe325`  
		Last Modified: Mon, 05 May 2025 17:34:51 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb44b0f60d0f2e264b4e84d0533e33807c0959829341314bad86b8c8aa7b17b1`  
		Last Modified: Mon, 05 May 2025 17:34:51 GMT  
		Size: 310.3 KB (310270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a86735363a8b94069fc4e440baf6ab80ab63f5af6539587ecaff59c6d7b98e`  
		Last Modified: Mon, 05 May 2025 17:34:50 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3391d2a01efc3c421b9bab859e5e7250e865618a137bcd2b6da4cdec66f754c2`  
		Last Modified: Mon, 05 May 2025 17:34:50 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba209b546131662cef9f0e229addcf58971af17f68894e18334bf52d4f08b95`  
		Last Modified: Mon, 05 May 2025 17:34:50 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e04890a83c56695270eac5222fc64d9de84c832020fa510ed221907bd5f77861`  
		Last Modified: Mon, 05 May 2025 17:35:01 GMT  
		Size: 209.2 MB (209214248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f6768314ead34460fa859d056b7fccfd7c8219e61a0da2113cc91bcb0307fb`  
		Last Modified: Mon, 05 May 2025 17:34:50 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
