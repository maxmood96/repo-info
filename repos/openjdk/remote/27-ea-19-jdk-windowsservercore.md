## `openjdk:27-ea-19-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:167b08d9453b420c717fff2887f7bafc89280b7c27e244ede655dc974ea1add2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `openjdk:27-ea-19-jdk-windowsservercore` - windows version 10.0.26100.32690; amd64

```console
$ docker pull openjdk@sha256:f14f9c613e4425d494c95c3d416f1a4016db113e4a19d76f24cf7e19e21a1b94
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2355738456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6d0a1b2e472bb92db680e44d108086a444efc3aabeeac775918c157ba181128`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Tue, 28 Apr 2026 23:42:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 28 Apr 2026 23:43:29 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 28 Apr 2026 23:43:29 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 28 Apr 2026 23:43:35 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 28 Apr 2026 23:43:36 GMT
ENV JAVA_VERSION=27-ea+19
# Tue, 28 Apr 2026 23:43:36 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/19/GPL/openjdk-27-ea+19_windows-x64_bin.zip
# Tue, 28 Apr 2026 23:43:37 GMT
ENV JAVA_SHA256=b2a6d883cbb261ccbc1f52e039ead30aa07359cc31cd35f3afe2101de05f06d1
# Tue, 28 Apr 2026 23:44:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 28 Apr 2026 23:44:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3642e4b8bb65ad3768f9f74a0dc48bb2e3294779b5d51573a234bfbe4f65324e`  
		Last Modified: Tue, 14 Apr 2026 18:48:19 GMT  
		Size: 606.9 MB (606926634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1a55a5afa17ab5e4c5a5fdec7a4b31c60e29e3660b1a4ef2dcf22e94d50a6d`  
		Last Modified: Tue, 28 Apr 2026 23:44:32 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc8837ed9daf277ac7052b445d7621a3c2a95d85fa667daa57b3b207afa24ec`  
		Last Modified: Tue, 28 Apr 2026 23:44:33 GMT  
		Size: 405.1 KB (405074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403f72a6ef8969568e74a4883772fa3b3f202e8f008423f3659db80f4dca41a7`  
		Last Modified: Tue, 28 Apr 2026 23:44:32 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a7850e9e2bd2c9c33933f11452fe27e560d00b37da2d9407c93660f90a99d2a`  
		Last Modified: Tue, 28 Apr 2026 23:44:33 GMT  
		Size: 387.4 KB (387387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0efad0c9640ae45e39e6620bbde2ff50eab3ee0c6265d62824e647bb0ee712c1`  
		Last Modified: Tue, 28 Apr 2026 23:44:30 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a032bc24847b99b0140eab919dfd927e9378fe07763562571bd689a81c6f986e`  
		Last Modified: Tue, 28 Apr 2026 23:44:31 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b2d65cd1f2c3f96e04bc64ff475a0acea1177e9f88f351d97579a3c70053bb`  
		Last Modified: Tue, 28 Apr 2026 23:44:30 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4661532f6b8a74e9f31ae1655f605386ff9b892f6936718ffbbbba18b410af4a`  
		Last Modified: Tue, 28 Apr 2026 23:44:47 GMT  
		Size: 225.0 MB (224952124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdce033e83cb7d02ba963fccdb5b6f659ee4ae670bfa2c208c856a0a8378cb0`  
		Last Modified: Tue, 28 Apr 2026 23:44:30 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-19-jdk-windowsservercore` - windows version 10.0.20348.5020; amd64

```console
$ docker pull openjdk@sha256:f5a6bbea05960f28b2e0d7a5a0cedcacb192eeff59ff42c921581cc8fdbb24ec
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2295930684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74743b98c5702f214259d67f684564de875de151f324e27f9bdacb277e5d40f0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 28 Apr 2026 23:38:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 28 Apr 2026 23:39:52 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 28 Apr 2026 23:39:53 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 28 Apr 2026 23:39:59 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 28 Apr 2026 23:40:00 GMT
ENV JAVA_VERSION=27-ea+19
# Tue, 28 Apr 2026 23:40:01 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/19/GPL/openjdk-27-ea+19_windows-x64_bin.zip
# Tue, 28 Apr 2026 23:40:02 GMT
ENV JAVA_SHA256=b2a6d883cbb261ccbc1f52e039ead30aa07359cc31cd35f3afe2101de05f06d1
# Tue, 28 Apr 2026 23:40:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 28 Apr 2026 23:40:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ca5032646149381c2c20fb699279519e0fd4478538cc8b6a7db546c3309a3c`  
		Last Modified: Tue, 28 Apr 2026 23:40:35 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5ad7d89f7255db4013281fd2f06d109f800d919a46511b6acb9db68854e922`  
		Last Modified: Tue, 28 Apr 2026 23:40:35 GMT  
		Size: 505.4 KB (505396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a73b7308558e7137ff6e276a65aebb343f17ecb840e1dfd07fb94d6b569d0e`  
		Last Modified: Tue, 28 Apr 2026 23:40:35 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f86bd08121523639d257dbdeeb133be64538d9018d508eb23776545f23c4eb`  
		Last Modified: Tue, 28 Apr 2026 23:40:35 GMT  
		Size: 317.3 KB (317274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f00bb232395193f3c84150e35b2764ebbeaece89a113ed6550d8fcf536023266`  
		Last Modified: Tue, 28 Apr 2026 23:40:33 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ef1f311c5948c909765d07005c50cf64f5ff9cf7147b148bb1e4a8b52e7d88`  
		Last Modified: Tue, 28 Apr 2026 23:40:33 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc8c5fd16ac7e31302e2098644aad2fe66f0f24d1b5ccfd6d60d306cd5905a2`  
		Last Modified: Tue, 28 Apr 2026 23:40:33 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb3152c43bc0a80b12c42d7d388648b2e27042ab4b3e1379daf609749c04c15`  
		Last Modified: Tue, 28 Apr 2026 23:40:50 GMT  
		Size: 224.9 MB (224888925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03393d9db90c01ace8792f004f68349055b0b3e022ecdb01a4b617c47630a6f7`  
		Last Modified: Tue, 28 Apr 2026 23:40:33 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
