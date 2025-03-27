## `openjdk:25-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:9ab844828e0036fdeb43a7a2ea3855eba90f363c89f377bb6a19dcf0cdce8cdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `openjdk:25-jdk-windowsservercore` - windows version 10.0.26100.3476; amd64

```console
$ docker pull openjdk@sha256:9656801fc3bd6d93a79b10c82e01ab00e5028fa6b92dec5eab39c38a74d977cc
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3117750808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad97a8b903e0242dddb4ecb4fdd432b74d0e80aeca65e37348af2ba0be30c63f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Thu, 27 Mar 2025 20:50:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 27 Mar 2025 20:50:34 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 27 Mar 2025 20:50:36 GMT
ENV JAVA_HOME=C:\openjdk-25
# Thu, 27 Mar 2025 20:50:46 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Thu, 27 Mar 2025 20:50:48 GMT
ENV JAVA_VERSION=25-ea+16
# Thu, 27 Mar 2025 20:50:51 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/16/GPL/openjdk-25-ea+16_windows-x64_bin.zip
# Thu, 27 Mar 2025 20:50:53 GMT
ENV JAVA_SHA256=147c12ac39a74d3d9e8372693e0531ab055aef0e9d4f8415efb5b4c3aa202353
# Thu, 27 Mar 2025 20:51:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 27 Mar 2025 20:51:15 GMT
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
	-	`sha256:0bdfee0f136698b08084ac718f853a570d218e748c0d5de53cc46c97de3ba302`  
		Last Modified: Thu, 27 Mar 2025 20:51:21 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600cae9ed8dd2ce2ceaa15084f7214fddb2c964e4c3bbb86cfa730cc5fe82045`  
		Last Modified: Thu, 27 Mar 2025 20:51:21 GMT  
		Size: 396.7 KB (396711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b2c200d20156e83fcda7f29d7b43307f2595ced9549a0e1b04152687cb189b2`  
		Last Modified: Thu, 27 Mar 2025 20:51:21 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76213de0189f78fa65c21a3436f2cf0e43c949d7ad07e40ba78bb8b6e62d80f7`  
		Last Modified: Thu, 27 Mar 2025 20:51:21 GMT  
		Size: 379.9 KB (379881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc5f842bf9912338bc4ab017abee6167f0e12ecb5c2b19706f0096c0422efae`  
		Last Modified: Thu, 27 Mar 2025 20:51:20 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1b2c2ba81215f9a4b14410328c28f34bf495824364dc3da2d7576a938f509b`  
		Last Modified: Thu, 27 Mar 2025 20:51:20 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7913d4569ff834bd1b7852892882d12b02f2d35dbb641658b13b3c24501a6c3c`  
		Last Modified: Thu, 27 Mar 2025 20:51:20 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9024daa40049ba0b9a621bcde6c0f937e9c7d340294b7f112f5975b1cb6527a`  
		Last Modified: Thu, 27 Mar 2025 20:51:32 GMT  
		Size: 208.3 MB (208318523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a68bc05226c45f3cb56046e7f5cb732ffb611f4fd03d55d3b4b358a1a9e6bd5`  
		Last Modified: Thu, 27 Mar 2025 20:51:20 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-jdk-windowsservercore` - windows version 10.0.20348.3328; amd64

```console
$ docker pull openjdk@sha256:180d647f7fe4c0d1b7c44d78206ffdd761604f1f3b32b0be59601d76cd436b18
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2478934020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8941cb174da5674422e21877a2da17237764904cddafc9a03dcd67537d45e795`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Thu, 27 Mar 2025 20:45:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 27 Mar 2025 20:45:25 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 27 Mar 2025 20:45:26 GMT
ENV JAVA_HOME=C:\openjdk-25
# Thu, 27 Mar 2025 20:45:34 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Thu, 27 Mar 2025 20:45:35 GMT
ENV JAVA_VERSION=25-ea+16
# Thu, 27 Mar 2025 20:45:35 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/16/GPL/openjdk-25-ea+16_windows-x64_bin.zip
# Thu, 27 Mar 2025 20:45:36 GMT
ENV JAVA_SHA256=147c12ac39a74d3d9e8372693e0531ab055aef0e9d4f8415efb5b4c3aa202353
# Thu, 27 Mar 2025 20:45:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 27 Mar 2025 20:45:57 GMT
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
	-	`sha256:d6474f5054fc1dc1295feb1b6482c1debb01b9e92bc9c0112cc3cc330545fccf`  
		Last Modified: Thu, 27 Mar 2025 20:46:03 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea43c7979b2bface6b1d4fdb2e3a310f3617533a4dd75d6b15186686aa58eec`  
		Last Modified: Thu, 27 Mar 2025 20:46:04 GMT  
		Size: 361.4 KB (361393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ac27f44066ccded18509a832da78e2de360dee863dc67308cfa222a99d0431`  
		Last Modified: Thu, 27 Mar 2025 20:46:03 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dbb7740deb3d7a181372ac9fb6d2f0fc5631ffc674604573e9db06791789f0b`  
		Last Modified: Thu, 27 Mar 2025 20:46:04 GMT  
		Size: 346.7 KB (346666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da2029b57b5edafb4ee58211b2a00f8c585abeeeea12b7097c3bed494d07840`  
		Last Modified: Thu, 27 Mar 2025 20:46:01 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1e5c3e629d7d41fac994f6d7ad7483b0b6f4f786e346ee07cd9bba36141e50e`  
		Last Modified: Thu, 27 Mar 2025 20:46:01 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d2c9679a389ec5e468f40fd078b45a3b75c6c1a4e24bc749fef838d591dfe9b`  
		Last Modified: Thu, 27 Mar 2025 20:46:01 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a7cb1be01a5cc8728c8a60f1a74f97ff30e9e226e04310872e8ec776e1f5d14`  
		Last Modified: Thu, 27 Mar 2025 20:46:12 GMT  
		Size: 208.3 MB (208277094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb0954aceecafe72278b2a5b79a8b81c0693d74e57f3f31be71dbdbf4a4b98f`  
		Last Modified: Thu, 27 Mar 2025 20:46:01 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-jdk-windowsservercore` - windows version 10.0.17763.7009; amd64

```console
$ docker pull openjdk@sha256:0975a33bd41d6869a5ed476070619166860b46a2b7493793f16a8b0f7cd3b726
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2360578047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842160a9320d810a09771bee1e36fdc27089ca0e9a7c7524cb7a6e9b7f51030c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Thu, 27 Mar 2025 20:49:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 27 Mar 2025 20:49:41 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 27 Mar 2025 20:49:42 GMT
ENV JAVA_HOME=C:\openjdk-25
# Thu, 27 Mar 2025 20:49:48 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Thu, 27 Mar 2025 20:49:49 GMT
ENV JAVA_VERSION=25-ea+16
# Thu, 27 Mar 2025 20:49:50 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/16/GPL/openjdk-25-ea+16_windows-x64_bin.zip
# Thu, 27 Mar 2025 20:49:50 GMT
ENV JAVA_SHA256=147c12ac39a74d3d9e8372693e0531ab055aef0e9d4f8415efb5b4c3aa202353
# Thu, 27 Mar 2025 20:50:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 27 Mar 2025 20:50:14 GMT
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
	-	`sha256:02d6eca61bde79d3da123bd60d2a8c875d9185959e21e3e736bd67e7c6350188`  
		Last Modified: Thu, 27 Mar 2025 20:50:22 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0429d3570729c075b688947838193e2c0c991af662f456325fd3bab5906c15a`  
		Last Modified: Thu, 27 Mar 2025 20:50:22 GMT  
		Size: 340.5 KB (340484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f8165eca826e23f850d4ee9ca1cedbc2fe008d7aba52c583c365e490750efe1`  
		Last Modified: Thu, 27 Mar 2025 20:50:22 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3998261fafdc38f53d5c5091631335c7a70bfd1a5cfb94733dbb95f3c55fd06`  
		Last Modified: Thu, 27 Mar 2025 20:50:22 GMT  
		Size: 331.5 KB (331459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f884f24a2f6bfd2354b9adcc9ba2c577f89e7a6a18d0a1b0a6964059100af3c2`  
		Last Modified: Thu, 27 Mar 2025 20:50:20 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b93595cc99fa3a59b256e0b9b5f203a1cba9b6a96d08a03e99d8c67a85105f34`  
		Last Modified: Thu, 27 Mar 2025 20:50:20 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07b086a1928cda62bf8efa0f60a4b6a019d0fecefcc37973f3a55d051717632`  
		Last Modified: Thu, 27 Mar 2025 20:50:20 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e488437b7789dea3e295e2fafa68a392841f741fff17e94b3dbe7badeac4b3`  
		Last Modified: Thu, 27 Mar 2025 20:50:32 GMT  
		Size: 208.3 MB (208263700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250a86624515bee6826e2f2901495fc36d2f4076cfd40f2ae829eb5103673acf`  
		Last Modified: Thu, 27 Mar 2025 20:50:20 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
