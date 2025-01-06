## `openjdk:25-ea-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:9e56df7c724c83cf4ff17be1c5afb9834b76f0636978b96ff770d3092f05c969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `openjdk:25-ea-jdk-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull openjdk@sha256:88374ac143c7527090ed555b948c57492daac4e5be913b6ce097726c8111ef8c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2223939780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e16cd2464c19e24f77842612c73edee91df71db2ea5228223ac7ebd4c565f2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Sat, 14 Dec 2024 00:29:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 14 Dec 2024 00:31:46 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 14 Dec 2024 00:31:46 GMT
ENV JAVA_HOME=C:\openjdk-25
# Sat, 14 Dec 2024 00:31:57 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 14 Dec 2024 00:31:58 GMT
ENV JAVA_VERSION=25-ea+2
# Sat, 14 Dec 2024 00:31:58 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/2/GPL/openjdk-25-ea+2_windows-x64_bin.zip
# Sat, 14 Dec 2024 00:31:59 GMT
ENV JAVA_SHA256=101667d00e2754bcb544ad7b59fb8ef62adc3acc1f762e71fb127d9633664020
# Sat, 14 Dec 2024 00:32:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 14 Dec 2024 00:32:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff98a2198e28ac82817c7f11797e3af5debe50cb39d6cb649eae8ccfd9b61d3`  
		Last Modified: Sat, 14 Dec 2024 00:32:43 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d4a8e9a9cb8a83056fff5ecc9c0ddfa7ded6b72eede1c5395c7bdd1135b8d7`  
		Last Modified: Sat, 14 Dec 2024 00:32:43 GMT  
		Size: 476.6 KB (476634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74978e0c5a91afbebb84fbd93bef83ad40b40f4ad7e139287c2ac9a4be9c60f6`  
		Last Modified: Sat, 14 Dec 2024 00:32:43 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73d72523319c64da1215ed152a16b6796c5e6496ce97cd871eb266793aa4871`  
		Last Modified: Sat, 14 Dec 2024 00:32:43 GMT  
		Size: 333.5 KB (333481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892710e4ce3674343777421e815488e01ae83c79bd1cfd2efec6d3a532616801`  
		Last Modified: Sat, 14 Dec 2024 00:32:41 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8d0e64cab182b2c47438153bc3ae1bc7999717684f2fd7690128602f9e0b93`  
		Last Modified: Sat, 14 Dec 2024 00:32:41 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:650e06309a7ee857f208e599d0340e6dfb60616e78ae619cdc20438c802c6867`  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f931047b0d85e4b89a59e2015927b895eb722b3380dfba9086044e605ea28660`  
		Last Modified: Sat, 14 Dec 2024 00:32:52 GMT  
		Size: 209.0 MB (208951706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d032faedcfc7d86c83c5ddb93e966f5b9b74b79473c1abde3b4a0bf4006d5ba`  
		Last Modified: Sat, 14 Dec 2024 00:32:41 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
