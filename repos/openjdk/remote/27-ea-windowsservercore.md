## `openjdk:27-ea-windowsservercore`

```console
$ docker pull openjdk@sha256:c3ce1aee42faf662ed674f4f70a47e9553268d03970c6368ea0af018d61e14a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32995; amd64
	-	windows version 10.0.20348.5256; amd64

### `openjdk:27-ea-windowsservercore` - windows version 10.0.26100.32995; amd64

```console
$ docker pull openjdk@sha256:4cfa3dfc7402b06cef63f87ac2298cab8f32a511da93dfa6212f4cdd322f7b3b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2503390745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f01eb7615ea8578b2ec76a52d2d810af92f361a9ac17a1beffdf15797576f44`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Tue, 16 Jun 2026 23:36:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 16 Jun 2026 23:38:07 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 16 Jun 2026 23:38:09 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 16 Jun 2026 23:38:16 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 16 Jun 2026 23:38:18 GMT
ENV JAVA_VERSION=27-ea+26
# Tue, 16 Jun 2026 23:38:19 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/26/GPL/openjdk-27-ea+26_windows-x64_bin.zip
# Tue, 16 Jun 2026 23:38:21 GMT
ENV JAVA_SHA256=007c293206270ff1040e9d27b573b2c3373cecfe97da2798206c6c1000cab9b9
# Tue, 16 Jun 2026 23:38:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 16 Jun 2026 23:38:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee71d57b2226db82d002abc39a97b7dd144f007db435566364a0285bf115b83`  
		Last Modified: Tue, 09 Jun 2026 18:08:12 GMT  
		Size: 756.1 MB (756083682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c84207d2f29da7d2ed1ade6ab2c507b5916f6cf31dc8b1e8c2047ae7ef14981`  
		Last Modified: Tue, 16 Jun 2026 23:38:57 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:349b129462ce906466f183f33e00b3e82dde9ae4fd94ff347ace84e9f95669df`  
		Last Modified: Tue, 16 Jun 2026 23:38:57 GMT  
		Size: 374.4 KB (374421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf34087564aae4dbabfb4d3624b6d84ca807f214e7e98d1f45a38267127353b`  
		Last Modified: Tue, 16 Jun 2026 23:38:57 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb245c587f59fb922b32f32954b860ec9084188d7586564e5bf97788f123e2d7`  
		Last Modified: Tue, 16 Jun 2026 23:38:57 GMT  
		Size: 363.9 KB (363932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52f20036f5392dacf421d9993902ee4fd18c630a6ff2dc0fff85c198ae208a1`  
		Last Modified: Tue, 16 Jun 2026 23:38:55 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a63beb1dc63407b7e973d4d10a65e73b693a06fd5995551f93c2643450db909a`  
		Last Modified: Tue, 16 Jun 2026 23:38:55 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc7103f9708b843c95a3ad97c975455617ac9397714bb8ea0fc9ab5c0394ccc1`  
		Last Modified: Tue, 16 Jun 2026 23:38:55 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363dcdc08548628e656b87afdbc627715f41df65dd7df52efde31de45c694f35`  
		Last Modified: Tue, 16 Jun 2026 23:39:11 GMT  
		Size: 223.5 MB (223501661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d58494ead237df8430ff6d6126fcfd3a26c0ee44d9678ccc57786d6af8119c`  
		Last Modified: Tue, 16 Jun 2026 23:38:55 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-windowsservercore` - windows version 10.0.20348.5256; amd64

```console
$ docker pull openjdk@sha256:5607221675381f71e0d03e6b7aabc78b419487fa6fe2bdf4070d6832610f4071
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2356473573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dd996cfc871d89092b53d578f28fe0378633ee31a691e8c3a508c7c8de4b22c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Tue, 16 Jun 2026 23:36:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 16 Jun 2026 23:37:11 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 16 Jun 2026 23:37:11 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 16 Jun 2026 23:37:18 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 16 Jun 2026 23:37:18 GMT
ENV JAVA_VERSION=27-ea+26
# Tue, 16 Jun 2026 23:37:19 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/26/GPL/openjdk-27-ea+26_windows-x64_bin.zip
# Tue, 16 Jun 2026 23:37:20 GMT
ENV JAVA_SHA256=007c293206270ff1040e9d27b573b2c3373cecfe97da2798206c6c1000cab9b9
# Tue, 16 Jun 2026 23:37:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 16 Jun 2026 23:37:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b0a4afae3a545d319d331a1cb04b65d0feee8e1c13d805952ae20e027bb71a`  
		Last Modified: Tue, 16 Jun 2026 23:37:53 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5204caebefdfb83ba2e72b15d73b29b21c1768f2a4b4bab044718b3f3f4b0d`  
		Last Modified: Tue, 16 Jun 2026 23:37:54 GMT  
		Size: 501.9 KB (501929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1feefb3ebcbea5ba996e4b8cc40e7891326eac3aee85a6d0f5ea9ef206d3eb`  
		Last Modified: Tue, 16 Jun 2026 23:37:53 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48a72387641273fd5db286bc3ff214bf9c4f7fe9f12a531aa734bbb50964bcc`  
		Last Modified: Tue, 16 Jun 2026 23:37:53 GMT  
		Size: 352.1 KB (352102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3615f15e97fc6b33ed0f0dd9161e1f539a1350f7c70a3eaae42ca509322bfa15`  
		Last Modified: Tue, 16 Jun 2026 23:37:52 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170989af0643076fb6e4a9d47f0d83a6ae4db2d86fcd7f225354f1793c6c9cb1`  
		Last Modified: Tue, 16 Jun 2026 23:37:52 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd16e031ac323eb77ec7d6d208b5e6ad8f04468f6ee1953ea08310a64de3b015`  
		Last Modified: Tue, 16 Jun 2026 23:37:51 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb97e47315290859fe018c537ef909894203668c243b73b090ca0182d8b7d9ec`  
		Last Modified: Tue, 16 Jun 2026 23:38:07 GMT  
		Size: 223.5 MB (223486131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff32ddb4474b999175b2d17980b710c6abf2164f1c6967a8152956b2568df07d`  
		Last Modified: Tue, 16 Jun 2026 23:37:51 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
