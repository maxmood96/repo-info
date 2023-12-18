## `openjdk:22-windowsservercore`

```console
$ docker pull openjdk@sha256:7bf046f647b1961811f2deeba7815a1c2ec05b83cc2552079ab7d0d57c8316aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2159; amd64
	-	windows version 10.0.17763.5206; amd64

### `openjdk:22-windowsservercore` - windows version 10.0.20348.2159; amd64

```console
$ docker pull openjdk@sha256:bef5ce7d33a924fac460444dabbd91a73c748c8eb8b9d37f7a10d53950fe719d
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2087824212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1908ee407bc1312ae975c3627ea731b3914ed99c40619cd08b4e23f8c757d4e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 02 Dec 2023 12:42:56 GMT
RUN Install update 10.0.20348.2159
# Sat, 16 Dec 2023 02:00:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 16 Dec 2023 02:00:54 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 16 Dec 2023 02:00:54 GMT
ENV JAVA_HOME=C:\openjdk-22
# Sat, 16 Dec 2023 02:01:00 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 16 Dec 2023 02:01:00 GMT
ENV JAVA_VERSION=22-ea+28
# Sat, 16 Dec 2023 02:01:01 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/28/GPL/openjdk-22-ea+28_windows-x64_bin.zip
# Sat, 16 Dec 2023 02:01:02 GMT
ENV JAVA_SHA256=8b5891a6ecb674efd45d31be04fb08d9b87cad241b943be0f4a9c9a1fbfda82f
# Sat, 16 Dec 2023 02:01:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 16 Dec 2023 02:01:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7839fc47f6e056f9e09a214230f8b7115e69419dbc74acbbb1ad6bc0caa28862`  
		Last Modified: Tue, 12 Dec 2023 18:27:40 GMT  
		Size: 500.7 MB (500674814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7ed59f58f8d6c9a44f799ad639f60c3f20a89f616e4f853c02728e626e5544`  
		Last Modified: Sat, 16 Dec 2023 02:01:28 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f178faf0763a8600afbf01dcf3f9207eac1789c64b1e8ff28584bb2105669e09`  
		Last Modified: Sat, 16 Dec 2023 02:01:28 GMT  
		Size: 495.1 KB (495064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f0153ca14a0b8956895e5e81f3dc7eab4daaaf980e5d01f9117169e57ebc20`  
		Last Modified: Sat, 16 Dec 2023 02:01:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348ac84660e161c7801dbe4848e900767eb0fc547520eb520f9021c5d8ae5473`  
		Last Modified: Sat, 16 Dec 2023 02:01:28 GMT  
		Size: 347.6 KB (347598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84dc9796ec2997c8a89ec42b8df901f108047f60f873d0cb1fca03b6eead95ec`  
		Last Modified: Sat, 16 Dec 2023 02:01:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d94001274265ebc86738194d6525e7f885a5c0fe479f13693c3e6cb0f2b6193`  
		Last Modified: Sat, 16 Dec 2023 02:01:27 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb74f15098fd4053fc60e8bbfc90b9a88a33d06e53ef717aa9b66ded0f8857d2`  
		Last Modified: Sat, 16 Dec 2023 02:01:27 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6ba6b1a71aaaa1ace032bf8295fe4ca190eab43cd04eb51c7a142b0e107341`  
		Last Modified: Sat, 16 Dec 2023 02:01:39 GMT  
		Size: 197.7 MB (197700206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2115009597075b6383bd896546b6172121d677217c7b2eaf4dc1de0292bb243b`  
		Last Modified: Sat, 16 Dec 2023 02:01:27 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-windowsservercore` - windows version 10.0.17763.5206; amd64

```console
$ docker pull openjdk@sha256:d7f478607e461ef574f7a7a32ace3d17c2cc79a5f9014556367399bb7010baa8
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2258328192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd36b63c92885ce91e235a0610f99dc04950bf0e097aa229fa3c182c49c34fb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Dec 2023 11:24:49 GMT
RUN Install update 10.0.17763.5206
# Sat, 16 Dec 2023 02:00:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 16 Dec 2023 02:01:18 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 16 Dec 2023 02:01:19 GMT
ENV JAVA_HOME=C:\openjdk-22
# Sat, 16 Dec 2023 02:01:41 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 16 Dec 2023 02:01:41 GMT
ENV JAVA_VERSION=22-ea+28
# Sat, 16 Dec 2023 02:01:42 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/28/GPL/openjdk-22-ea+28_windows-x64_bin.zip
# Sat, 16 Dec 2023 02:01:43 GMT
ENV JAVA_SHA256=8b5891a6ecb674efd45d31be04fb08d9b87cad241b943be0f4a9c9a1fbfda82f
# Sat, 16 Dec 2023 02:02:25 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 16 Dec 2023 02:02:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35ae5ad761bfd7e5fb48c234de8722eaa28e17e2c956816fecb417ab6259c29`  
		Last Modified: Tue, 12 Dec 2023 19:14:24 GMT  
		Size: 409.1 MB (409088642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55be67c91d932a702980bd1a76388f6f069b58071dddf74c18d691104e88e82b`  
		Last Modified: Sat, 16 Dec 2023 02:02:33 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833b6581bf1f9dd2f06c0fccb0b251b3a690ef1781444f82ba8fc19b9eb4209f`  
		Last Modified: Sat, 16 Dec 2023 02:02:34 GMT  
		Size: 517.5 KB (517486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6160367c6fd66fac96977261069163f13cb57a2b853f192206483c9e69350255`  
		Last Modified: Sat, 16 Dec 2023 02:02:33 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eff0168fda73f3b55e6c349a5e8cefc2267357d88abca9b4ac5a0969c3c5914`  
		Last Modified: Sat, 16 Dec 2023 02:02:33 GMT  
		Size: 362.5 KB (362494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eddbab60482ee60bacacf895c4bf9f2c4484e64c2b7842ebfbe6b2752d7241d`  
		Last Modified: Sat, 16 Dec 2023 02:02:30 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66d9dfe54f934d49f612bd29739e75f318490c4443b47e6c696382b3a4bd0a51`  
		Last Modified: Sat, 16 Dec 2023 02:02:30 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ece9cf06fb96ed286ee3cfa3ded12e34aeab89399d11ad7bd72f19ce82cdb4`  
		Last Modified: Sat, 16 Dec 2023 02:02:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6650722e37096dfeae7235d2a3c6e26f5c3c10a354aeca09f6eb557ddf3127b2`  
		Last Modified: Sat, 16 Dec 2023 02:02:42 GMT  
		Size: 197.7 MB (197731424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19650fadab3559954db508e855bbeddb66e5cb2506875361963f72e20ca2c798`  
		Last Modified: Sat, 16 Dec 2023 02:02:30 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
