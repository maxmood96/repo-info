## `openjdk:25-ea-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:cade2b1aa5f8892648abfcf2859a4d0ecf79c84a0afee1f155055bb7324ac1ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `openjdk:25-ea-windowsservercore-ltsc2025` - windows version 10.0.26100.3476; amd64

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
