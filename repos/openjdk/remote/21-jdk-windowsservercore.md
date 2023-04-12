## `openjdk:21-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:1adfa67e352bed7425218a979e771a95095717a7b43c567364798da511c1ac0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1668; amd64
	-	windows version 10.0.17763.4252; amd64

### `openjdk:21-jdk-windowsservercore` - windows version 10.0.20348.1668; amd64

```console
$ docker pull openjdk@sha256:b958816d276423c868703d99f790eac872e4641bc743cdedfc188a2404efb10b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1960521486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57e57783e9ef953e4ea0baa32f009a7ca2359e43cafd07ce1e4208bd20c04f47`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Wed, 05 Apr 2023 00:38:27 GMT
RUN Install update 10.0.20348.1668
# Tue, 11 Apr 2023 23:37:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Apr 2023 23:38:34 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 11 Apr 2023 23:38:35 GMT
ENV JAVA_HOME=C:\openjdk-21
# Tue, 11 Apr 2023 23:39:38 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 11 Apr 2023 23:39:39 GMT
ENV JAVA_VERSION=21-ea+17
# Tue, 11 Apr 2023 23:39:39 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk21/17/GPL/openjdk-21-ea+17_windows-x64_bin.zip
# Tue, 11 Apr 2023 23:39:40 GMT
ENV JAVA_SHA256=d3393a8337621852f355aac733539233e60e2f21e24d01da4858bd7fe583ff02
# Tue, 11 Apr 2023 23:40:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 11 Apr 2023 23:40:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ecfa9c953d28a9da9d422b57cd0361c57c44e1faaaed7e50a2537d1c29cee1`  
		Last Modified: Wed, 12 Apr 2023 00:50:33 GMT  
		Size: 376.6 MB (376573004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98474c9b39bb0e3a2d79dca81a90952011b65d1fa352021dacd30335d1bb69f4`  
		Last Modified: Wed, 12 Apr 2023 00:49:03 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5267a6534dbac53b3d9701ccd066e434901994c544b2dab38b384ba337c288`  
		Last Modified: Wed, 12 Apr 2023 00:49:04 GMT  
		Size: 756.8 KB (756811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec944a3e06641c097fd1420f03d6ca79e689d4e7e7567d6d5220e5722f63c4b`  
		Last Modified: Wed, 12 Apr 2023 00:49:03 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0fe5145f5a0cc66a5c1d0123eeea45b9ec36dfa42ccfe03d869d89a7bd8416`  
		Last Modified: Wed, 12 Apr 2023 00:49:04 GMT  
		Size: 530.6 KB (530559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97897c6858bdba58174f05baa91597b779ee6c575c5a75379aeef64a77f263ab`  
		Last Modified: Wed, 12 Apr 2023 00:49:01 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b3d4d46fab2fa7d1221c086a84f50830882b7f28a0c066220b482d5e3c6279`  
		Last Modified: Wed, 12 Apr 2023 00:49:01 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cd2ef1ddf19a0824625d69039db669a9735720b9533b952a285bc9b6667e262`  
		Last Modified: Wed, 12 Apr 2023 00:49:01 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb87a32b1abb071125a70c26c87558dbca48e4ea9615a44c024d22857ca245b`  
		Last Modified: Wed, 12 Apr 2023 00:49:32 GMT  
		Size: 196.6 MB (196623466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404bc825672d2584e919fcbffe1052fbd5a59e313485409e6dc7f97892ec7dc0`  
		Last Modified: Wed, 12 Apr 2023 00:49:01 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-jdk-windowsservercore` - windows version 10.0.17763.4252; amd64

```console
$ docker pull openjdk@sha256:883fac92d22335b58ee0832ade7ebe51fd997b9ac7bb5548ecc597237a47f644
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2268502674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d4f2d387575e5f8ebbdabb68ccb3c450d1b114fd9b75e57a0d47816c67767e9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Wed, 05 Apr 2023 00:41:54 GMT
RUN Install update 10.0.17763.4252
# Tue, 11 Apr 2023 23:40:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Apr 2023 23:42:24 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 11 Apr 2023 23:42:25 GMT
ENV JAVA_HOME=C:\openjdk-21
# Tue, 11 Apr 2023 23:43:30 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 11 Apr 2023 23:43:31 GMT
ENV JAVA_VERSION=21-ea+17
# Tue, 11 Apr 2023 23:43:32 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk21/17/GPL/openjdk-21-ea+17_windows-x64_bin.zip
# Tue, 11 Apr 2023 23:43:33 GMT
ENV JAVA_SHA256=d3393a8337621852f355aac733539233e60e2f21e24d01da4858bd7fe583ff02
# Tue, 11 Apr 2023 23:45:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 11 Apr 2023 23:45:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9094c39c4b36a86359abb3da9e9d0d9c69b6930e9c7b308120310d43d63f693`  
		Last Modified: Wed, 12 Apr 2023 00:52:10 GMT  
		Size: 363.3 MB (363347289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9103f1e2cdefe8f16dae9619b88e38aa659abb17276d2362d435ad0721d3bf41`  
		Last Modified: Wed, 12 Apr 2023 00:50:55 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2a17e347e3144ab020e098f925bc273e89f499e03114bea80260a0bc601f9c`  
		Last Modified: Wed, 12 Apr 2023 00:50:56 GMT  
		Size: 487.7 KB (487655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c03d658bc6a61ee9591db424ef2db8137173e1ff03e628327eda8134490cb46`  
		Last Modified: Wed, 12 Apr 2023 00:50:55 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4c3c308ea664c1238fc40d20ade9c94a79f29169edf764c414e542fc4495ab`  
		Last Modified: Wed, 12 Apr 2023 00:50:55 GMT  
		Size: 311.4 KB (311449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc6c5f10c1d9914baa29bc43f83e428b917b26cd7675e79cb6cba4960d9a323`  
		Last Modified: Wed, 12 Apr 2023 00:50:53 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7cc9538138f333a3d84ce9717025319bc8f75cdae14388944b26c8a0257d58b`  
		Last Modified: Wed, 12 Apr 2023 00:50:53 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d63a6bd79d53c4a2527e5a2c7305b4edfb3de03312520405f05b896c4fc2c9`  
		Last Modified: Wed, 12 Apr 2023 00:50:53 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a26f5b7e8b15f1b7c9355024b9ddd29b0cca06b6bc07880a75b9e09954831d7`  
		Last Modified: Wed, 12 Apr 2023 00:51:22 GMT  
		Size: 196.4 MB (196403791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cbea611c66192cb8c10c7fd44597c01f8066666168e0c921761eec925eabe94`  
		Last Modified: Wed, 12 Apr 2023 00:50:53 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
