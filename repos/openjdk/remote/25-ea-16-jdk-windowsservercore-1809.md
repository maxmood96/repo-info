## `openjdk:25-ea-16-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:7c54b1149048b7b5e92e0525a050332d65880be479f3c8df40f80a082d253bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `openjdk:25-ea-16-jdk-windowsservercore-1809` - windows version 10.0.17763.7009; amd64

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
