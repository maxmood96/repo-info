## `openjdk:27-ea-19-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:7fcab37ae6157cae55e19a792f1c48488dddc07053aac0b9682dd31056901d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32690; amd64

### `openjdk:27-ea-19-windowsservercore-ltsc2025` - windows version 10.0.26100.32690; amd64

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
