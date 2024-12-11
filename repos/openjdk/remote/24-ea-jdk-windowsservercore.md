## `openjdk:24-ea-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:a2789c0111072af1a03092354336fcf53a210608e75d7f98a1376b14c0171667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `openjdk:24-ea-jdk-windowsservercore` - windows version 10.0.20348.2966; amd64

```console
$ docker pull openjdk@sha256:609d675179052acbc474a4bf7d4058ca97bdd170f441da43dc4f2974fd0d4bf4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2463366905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539db919545665edc951b64b63cd67ad76a8c5e0c4b7379ded4f34de105362ce`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:41:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:41:55 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:41:55 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 11 Dec 2024 20:42:01 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:42:01 GMT
ENV JAVA_VERSION=24-ea+27
# Wed, 11 Dec 2024 20:42:02 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/27/GPL/openjdk-24-ea+27_windows-x64_bin.zip
# Wed, 11 Dec 2024 20:42:02 GMT
ENV JAVA_SHA256=d3c4c15520262f2d3de174d973e37053081a8b627a66e8f4939419b4af8b4823
# Wed, 11 Dec 2024 20:42:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:42:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d74e940fc5c564d16836ce79ac9032f9de9b429e607886f8a884fa65282a21`  
		Last Modified: Wed, 11 Dec 2024 20:42:25 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3087335ca7385e68c6c4288a0c0a8e61933e24deffc451ac5bf3a9602b4b1a9a`  
		Last Modified: Wed, 11 Dec 2024 20:42:25 GMT  
		Size: 346.6 KB (346633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58b5db76e23a40bb6014b521a0b30ca1fc45be61fa67b7bea7baf4566f33104`  
		Last Modified: Wed, 11 Dec 2024 20:42:24 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11653d8d8ddf22f9a59ccd1373fb768eea13e1ab4425aa780607453858117389`  
		Last Modified: Wed, 11 Dec 2024 20:42:25 GMT  
		Size: 334.2 KB (334225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a1a922bce3d8ed0f3eb41cdac053b27993568fa93822d8b818fab8cc99093f`  
		Last Modified: Wed, 11 Dec 2024 20:42:23 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2851f4d0d423d7b95515938780361333d80075d0c515a4af02dc1ebc47d09f07`  
		Last Modified: Wed, 11 Dec 2024 20:42:24 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed62fc0ef63c50b67bbdf3d6aea957f6b08bd682c40ddc2c0529adb194a0bab`  
		Last Modified: Wed, 11 Dec 2024 20:42:23 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3988f1adfadc5e7ebe2adb8cccae758b2e034006a85f8d86df61907f0d38116c`  
		Last Modified: Wed, 11 Dec 2024 20:42:36 GMT  
		Size: 208.8 MB (208804703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2130ecc335238637eb1727bace20766a37671dff7b9124b09d54e324b3c4b2b`  
		Last Modified: Wed, 11 Dec 2024 20:42:24 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-ea-jdk-windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull openjdk@sha256:a09a2ffa780177ab5bf8ac6c13e60c37e4e0695eb65cf4fe2b942091acab1960
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2223767629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df7b20c8e45cf6eda6e2a18e7a8bdc3a6e19d1d4c04aad8c5138c366dee00609`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:41:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:42:01 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:42:02 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 11 Dec 2024 20:42:08 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:42:08 GMT
ENV JAVA_VERSION=24-ea+27
# Wed, 11 Dec 2024 20:42:09 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/27/GPL/openjdk-24-ea+27_windows-x64_bin.zip
# Wed, 11 Dec 2024 20:42:09 GMT
ENV JAVA_SHA256=d3c4c15520262f2d3de174d973e37053081a8b627a66e8f4939419b4af8b4823
# Wed, 11 Dec 2024 20:42:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:42:35 GMT
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
	-	`sha256:ae6d1ef957c650f08c7568fe39557373187299b3d48893d17035cff048509c3c`  
		Last Modified: Wed, 11 Dec 2024 20:42:42 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d9dbec08674eb0861c52c8aa12db8e14c3c22ee86d2c14923931616327fc899`  
		Last Modified: Wed, 11 Dec 2024 20:42:42 GMT  
		Size: 464.8 KB (464782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5797b61019665b45273eddd365ad0216d047220cb3ab7067e25e8740300dec`  
		Last Modified: Wed, 11 Dec 2024 20:42:42 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc19cd73d0ef1694f030fe61fa3610184a137162dcfc5f0c8d4f2cd8c0db6a52`  
		Last Modified: Wed, 11 Dec 2024 20:42:42 GMT  
		Size: 318.4 KB (318362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334173c65723d8fca67a7673e0671004f5fa1d5c4c18ec59b6fe97e856b25bf2`  
		Last Modified: Wed, 11 Dec 2024 20:42:40 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42083c1d9b42c3cb091c8b62b4b5cd3c4695e1882f832b0ea6250cd3b5ef10f6`  
		Last Modified: Wed, 11 Dec 2024 20:42:40 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83ab12b907cf4447072b4af411927f0dfd3aa4d81156cf37acba514618c9710c`  
		Last Modified: Wed, 11 Dec 2024 20:42:40 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b7617ed8ffe45cc8541c9b3ff910af1ef65b6ce3eacddc4c9a4d072a3a4f4a`  
		Last Modified: Wed, 11 Dec 2024 20:42:51 GMT  
		Size: 208.8 MB (208806510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813c43c369dc061ee1d2c9316c98cd401bae1792dc3a30d3bed1a87b7f952902`  
		Last Modified: Wed, 11 Dec 2024 20:42:40 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
