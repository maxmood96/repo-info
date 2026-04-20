## `openjdk:27-ea-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:7a00c8a3046a48bdcb6c2e7e12f88341a6324769400077f1d2f76c03d0f1d994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `openjdk:27-ea-jdk-windowsservercore` - windows version 10.0.26100.32690; amd64

```console
$ docker pull openjdk@sha256:69cd7b42a690284cff696e75a9b00451eea1bf94e75763c4b9ef8320b4dcf8e1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2355724563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a1ac017e229456b5240c3a1bfcdcd06b89599f500a0b3a268565c991a4c8d37`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Mon, 20 Apr 2026 17:46:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 20 Apr 2026 17:48:06 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 20 Apr 2026 17:48:07 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 20 Apr 2026 17:48:14 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 20 Apr 2026 17:48:14 GMT
ENV JAVA_VERSION=27-ea+18
# Mon, 20 Apr 2026 17:48:15 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/18/GPL/openjdk-27-ea+18_windows-x64_bin.zip
# Mon, 20 Apr 2026 17:48:16 GMT
ENV JAVA_SHA256=a1c0dd830438f8730b226f0088f5037f49def2c4f6b4e53d30434bbd790975a0
# Mon, 20 Apr 2026 17:48:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 20 Apr 2026 17:48:49 GMT
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
	-	`sha256:a5e9fc55d3681fcfea948c4cccb5189b5339b31efeda3a7f899e4d39f0dbd5ca`  
		Last Modified: Mon, 20 Apr 2026 17:48:55 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f4bca560debdeff044aea3085780da9a4202289ee7e099405163d5425dd87f`  
		Last Modified: Mon, 20 Apr 2026 17:48:55 GMT  
		Size: 416.4 KB (416376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77ca7292690544e587f74736e20eee93a1d853088aac3f918070dcce05fd213`  
		Last Modified: Mon, 20 Apr 2026 17:48:55 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b1c39a4437a6ed39ba03897d20a9da34a3b0ad6e1f5b7f08afabe104ed3b2c`  
		Last Modified: Mon, 20 Apr 2026 17:48:55 GMT  
		Size: 359.0 KB (358998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a938bef1ede485496ae1d283599d14eaca9af8f834545aba23e7b5f1b5162f`  
		Last Modified: Mon, 20 Apr 2026 17:48:53 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0023756868ba6046494f09f9d56f0aa9204fa1e5e220d3a816bed96c86b2f5`  
		Last Modified: Mon, 20 Apr 2026 17:48:53 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65e8cb2c1dcce47820af7e65905c47b5ab3b15d2604a29495ba073fbf1ef42b`  
		Last Modified: Mon, 20 Apr 2026 17:48:53 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49aee66e5b26e04f3bf39c9f60b3f85e3582e3ba1d196f2b7dbfdebba2bd9edc`  
		Last Modified: Mon, 20 Apr 2026 17:49:08 GMT  
		Size: 225.0 MB (224955285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9da037f5ba713c201fe9e025257444d62a5b049a76422d69789212cf65a7d59`  
		Last Modified: Mon, 20 Apr 2026 17:48:53 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-jdk-windowsservercore` - windows version 10.0.20348.5020; amd64

```console
$ docker pull openjdk@sha256:bd6719db65ece52dba86157db74db5d43d78a21e6aa8a468d93666e6779fc620
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2296025076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b5745fe3fba7c2e76f62e785ff2f39718d2808cb61fec8c79f89c727661b062`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Mon, 20 Apr 2026 17:46:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 20 Apr 2026 17:47:35 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 20 Apr 2026 17:47:36 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 20 Apr 2026 17:47:43 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 20 Apr 2026 17:47:44 GMT
ENV JAVA_VERSION=27-ea+18
# Mon, 20 Apr 2026 17:47:46 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/18/GPL/openjdk-27-ea+18_windows-x64_bin.zip
# Mon, 20 Apr 2026 17:47:47 GMT
ENV JAVA_SHA256=a1c0dd830438f8730b226f0088f5037f49def2c4f6b4e53d30434bbd790975a0
# Mon, 20 Apr 2026 17:49:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 20 Apr 2026 17:49:15 GMT
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
	-	`sha256:6a215123365f2e4a800dcbadbe6f4d77d41e6d6343e32a3af2c209aaf081cbed`  
		Last Modified: Mon, 20 Apr 2026 17:49:31 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdfc40daf4b59722e7041c02666b07c46ba45f34e6ee3c9c012bee357b129b7c`  
		Last Modified: Mon, 20 Apr 2026 17:49:32 GMT  
		Size: 505.1 KB (505084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b74ad720297a5ec6142e6735d38833ec741d3719e5efa72e9da765b26dc81743`  
		Last Modified: Mon, 20 Apr 2026 17:49:31 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620f4ec28b9cf60c1c18b0ba579b5e4ea813b0fe9a448cadfcc20c696f8e71cc`  
		Last Modified: Mon, 20 Apr 2026 17:49:31 GMT  
		Size: 341.3 KB (341294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48229954c79f8b145feac8c46260acc9fc4acd5cc503501c4fd070361c490f4f`  
		Last Modified: Mon, 20 Apr 2026 17:49:29 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346d8b04007d9371c69f340ed67f888836434167d246e473a7bf2da1b51e7594`  
		Last Modified: Mon, 20 Apr 2026 17:49:29 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3356a6e8d35a5577be565929909c30a19b16c21512ab2e47a3585b4e3016147`  
		Last Modified: Mon, 20 Apr 2026 17:49:29 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f626a7081f215319c58b187572903f52f08c1e5a7e06e01e213eea1b7b7d3ada`  
		Last Modified: Mon, 20 Apr 2026 17:49:43 GMT  
		Size: 225.0 MB (224959521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6ede1817bc1670957c5c2357dee2893ac9e7e586dc3add2b332113d1789d851`  
		Last Modified: Mon, 20 Apr 2026 17:49:29 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
