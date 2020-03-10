## `openjdk:13-jdk`

```console
$ docker pull openjdk@sha256:9e83e9ac5744418e6147d1953db10a4cd8a677811d4e0f609a83f2034d575e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	windows version 10.0.17763.1040; amd64
	-	windows version 10.0.14393.3506; amd64

### `openjdk:13-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:53cacd45e87d2e24e07143f73540e8aa40b31d9f52c6ee69ebffe7bd34bc8ca2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.9 MB (253869247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff31919fd91c62f64a0815e18cade1bb567ca2dde6b7d24b60a9ebbdcde365b7`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 30 Aug 2018 21:49:27 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Tue, 10 Mar 2020 02:20:39 GMT
ADD file:ca821d696bf87ff0b7ed9d85b5b0acc4656fc6498d2f5bd2c051bb16a99bfcbf in / 
# Tue, 10 Mar 2020 02:20:40 GMT
CMD ["/bin/bash"]
# Tue, 10 Mar 2020 02:37:57 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 10 Mar 2020 02:37:57 GMT
ENV LANG=en_US.UTF-8
# Tue, 10 Mar 2020 02:40:08 GMT
ENV JAVA_HOME=/usr/java/openjdk-13
# Tue, 10 Mar 2020 02:40:08 GMT
ENV PATH=/usr/java/openjdk-13/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2020 02:40:08 GMT
ENV JAVA_VERSION=13.0.2
# Tue, 10 Mar 2020 02:40:08 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk13.0.2/d4173c853231432d94f001e99d882ca7/8/GPL/openjdk-13.0.2_linux-x64_bin.tar.gz
# Tue, 10 Mar 2020 02:40:09 GMT
ENV JAVA_SHA256=acc7a6aabced44e62ec3b83e3b5959df2b1aa6b3d610d58ee45f0c21a7821a71
# Tue, 10 Mar 2020 02:40:34 GMT
RUN set -eux; 		curl -fL -o /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 	mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		java --version; 	javac --version
# Tue, 10 Mar 2020 02:40:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd17e56c322c9601c98f41573bb47bd4cd68ff386d7d07538f156a7c0ef6c650`  
		Last Modified: Tue, 10 Mar 2020 02:22:01 GMT  
		Size: 42.7 MB (42725735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecdd73bb99224b1c73d7d3d8eea56a91f5e7fc73628dcfa3b5432cca23c7373d`  
		Last Modified: Tue, 10 Mar 2020 02:42:14 GMT  
		Size: 14.8 MB (14770095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a00902ec9e71adeff6a5b90b0d6f0d3527baec74ca75174ed4bc05a0cf0e2b`  
		Last Modified: Tue, 10 Mar 2020 02:46:34 GMT  
		Size: 196.4 MB (196373417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:13-jdk` - windows version 10.0.17763.1040; amd64

```console
$ docker pull openjdk@sha256:17d3aeeda207b99eac2d7636d951104e7e5e8fd3e41c8ee18b5c0bd7d75e0014
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2426863924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70a64a3f8c3472e0854d9ab47330c369731d68e4f94ed43fc9f2df272938c24b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 17 Feb 2020 06:57:13 GMT
RUN Install update 1809-amd64
# Thu, 20 Feb 2020 01:13:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2020 01:14:33 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Thu, 20 Feb 2020 02:26:38 GMT
ENV JAVA_HOME=C:\openjdk-13
# Thu, 20 Feb 2020 02:27:04 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Thu, 20 Feb 2020 02:27:05 GMT
ENV JAVA_VERSION=13.0.2
# Thu, 20 Feb 2020 02:27:06 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk13.0.2/d4173c853231432d94f001e99d882ca7/8/GPL/openjdk-13.0.2_windows-x64_bin.zip
# Thu, 20 Feb 2020 02:27:08 GMT
ENV JAVA_SHA256=fab29dcfda6ca4af3a9b973ecdde61dafcd9b307cb9237c25d25b2633bb08084
# Thu, 20 Feb 2020 02:29:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 20 Feb 2020 02:29:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b5405b7580792436b60c664b5fa766ea57f5a60c1d9a8c522cf53e99e4813355`  
		Size: 695.8 MB (695818606 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2061e035d6ba931d9f00238104b970d3410f4ef0d9603b4f074c7052858e01e3`  
		Last Modified: Thu, 20 Feb 2020 03:03:21 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f0782e4992ed8796b0b5659aad759ed2fb47d4fafaaa5a38afe4f993f94d68`  
		Last Modified: Thu, 20 Feb 2020 03:03:23 GMT  
		Size: 4.6 MB (4567940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6794e8c0f027abf0ff77465508a19da18b7bc0b1639c6f62c9f4cbe67269893`  
		Last Modified: Thu, 20 Feb 2020 03:16:06 GMT  
		Size: 1.2 KB (1199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:225303d7c23e84e24c75d316bf245263ae2eb8e01acfc1f6dc206400eda27339`  
		Last Modified: Thu, 20 Feb 2020 03:16:06 GMT  
		Size: 291.5 KB (291506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0abd8c5b4b0fc762adbd4a34df65bb6f5985043a5af51a932e70b35e4449202d`  
		Last Modified: Thu, 20 Feb 2020 03:16:03 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a4c1021f6cb2eecbd7fdc53120d89db9752a2e467b8f1f40445d88e1d90303a`  
		Last Modified: Thu, 20 Feb 2020 03:16:03 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff3ccf206912545099079822870aab3c3766ad458dc1126d4d416f6f61d83b94`  
		Last Modified: Thu, 20 Feb 2020 03:16:03 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2ad802fc96663a43010d161155fa644ddaedd7ae18b3dc7ad94e6f2b0509ce`  
		Last Modified: Thu, 20 Feb 2020 03:16:26 GMT  
		Size: 191.5 MB (191493360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf3ebc8b543685ae7644f63bda7aafb2924eae2557621ef65bb0fc786816de01`  
		Last Modified: Thu, 20 Feb 2020 03:16:03 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:13-jdk` - windows version 10.0.14393.3506; amd64

```console
$ docker pull openjdk@sha256:ea1cd435a6b4a681321586aa0768c6ce939fbec5bd3cbd08665fec3c5c9e07b9
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5934295833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b4960f44d1ff3732f12869c39363b2bd22ac6fd5eecc46108951f46c28188a9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 01:48:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2020 01:49:57 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Thu, 20 Feb 2020 02:29:30 GMT
ENV JAVA_HOME=C:\openjdk-13
# Thu, 20 Feb 2020 02:30:50 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Thu, 20 Feb 2020 02:30:52 GMT
ENV JAVA_VERSION=13.0.2
# Thu, 20 Feb 2020 02:30:53 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk13.0.2/d4173c853231432d94f001e99d882ca7/8/GPL/openjdk-13.0.2_windows-x64_bin.zip
# Thu, 20 Feb 2020 02:30:55 GMT
ENV JAVA_SHA256=fab29dcfda6ca4af3a9b973ecdde61dafcd9b307cb9237c25d25b2633bb08084
# Thu, 20 Feb 2020 02:33:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 20 Feb 2020 02:33:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:72c4471958f7f0f07260f0f430bcffb0bc07811088c24cffba1439d250ea1ae3`  
		Last Modified: Thu, 20 Feb 2020 03:04:52 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6eada8556f1688b8cc14a7529ed2bd5822b6570a73c142f15a023eda1563d9`  
		Last Modified: Thu, 20 Feb 2020 03:04:58 GMT  
		Size: 5.4 MB (5361808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d7e0360db88022dc77287fe139b78440c1d15111c72bbd04433538e6b9bfcf`  
		Last Modified: Thu, 20 Feb 2020 03:17:48 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea41f29f83b3f804ed1b09788d29f4468d661c9687c90a5d0cfab12785819d0d`  
		Last Modified: Thu, 20 Feb 2020 03:17:50 GMT  
		Size: 5.3 MB (5343346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc89a22936073ef65d93f5a9b13070558353152f5e3504354ddb15c642c46d1`  
		Last Modified: Thu, 20 Feb 2020 03:17:46 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b22660344da3bd71f791ca03a985c0456ce4db4ffa630f6c7689ec1c43a736`  
		Last Modified: Thu, 20 Feb 2020 03:17:45 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a8f2b00dae04c6fb7f53885fa6ef6e34cf707d712d6f2de7ed51969dbc421d`  
		Last Modified: Thu, 20 Feb 2020 03:17:46 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5c781d8cdac0e5e1fc4ad7c8ecbd320df713c9ea56e69ba634778f841f99cf`  
		Last Modified: Thu, 20 Feb 2020 03:18:22 GMT  
		Size: 196.5 MB (196518638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364b71cb0fe629a710259cba1699ef9be7903ca0375369ead0044e1c4d06603e`  
		Last Modified: Thu, 20 Feb 2020 03:17:45 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
