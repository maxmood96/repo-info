## `openjdk:27-ea-jdk`

```console
$ docker pull openjdk@sha256:4b9a59623f19e7072e6c5655e3d525be6228ebd6d35352a356dfa87c5cba818e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `openjdk:27-ea-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:044e00e7d725c97bf09d62ac0be5c5715383bd92e521feadece148a1a19bd964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.7 MB (313677188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2879c4a8eabe2359074e4a0478fe01f8b476105fc51f084c687013e0a000782e`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Tue, 20 Jan 2026 18:46:27 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 20 Jan 2026 18:46:46 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 20 Jan 2026 18:46:46 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:46:46 GMT
ENV LANG=C.UTF-8
# Tue, 20 Jan 2026 18:46:46 GMT
ENV JAVA_VERSION=27-ea+5
# Tue, 20 Jan 2026 18:46:46 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/5/GPL/openjdk-27-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='2d85f5a6432abd2eb67b974ed1ab85d2a9557b06be285f2fc6e5d94429951468'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/5/GPL/openjdk-27-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='58f4450fff4f277000cf3d520a612275b0d9b6cb24e1287457d4651e98714b4a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 20 Jan 2026 18:46:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:49 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b5c65ef8298a36f2091528dbc70ce16fb2b685fe9e234aa80bca9294ddb27f1`  
		Last Modified: Tue, 20 Jan 2026 18:47:10 GMT  
		Size: 38.3 MB (38296097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74cb17f06827a1bc4df9d04cbc37bef169d7852266770da1be1a3dcdcd75c818`  
		Last Modified: Tue, 20 Jan 2026 18:56:16 GMT  
		Size: 228.1 MB (228066553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:bba8ae143115ea33ee3e0aa829a696ed4c083c04f4a8f45760aa98d02308d059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6340f8a01a0d70bf344d12e1d82a809915665d818a9b7c9f72270c06aa3b077d`

```dockerfile
```

-	Layers:
	-	`sha256:03fccd02d5aeb1dfcb45673e60e8e17350aa807c422318e6504f9d92dcbc1a00`  
		Last Modified: Tue, 20 Jan 2026 18:47:08 GMT  
		Size: 3.7 MB (3655355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c3eb66a3e293b7bdd85bd5ad8ca2b5c2448cae9c4cc4507f9d48d9dbaf84726`  
		Last Modified: Tue, 20 Jan 2026 18:47:08 GMT  
		Size: 17.8 KB (17814 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f78f244bfca1718a51e097ad984f9d6211f8d9755b16b6554cc5ceb82f1396ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310599400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a53943beec9fd811937b6451011dc432a3f09d3b109084bfe3320a714d8b9ae`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Tue, 20 Jan 2026 18:47:31 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 20 Jan 2026 18:47:41 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 20 Jan 2026 18:47:41 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:47:41 GMT
ENV LANG=C.UTF-8
# Tue, 20 Jan 2026 18:47:41 GMT
ENV JAVA_VERSION=27-ea+5
# Tue, 20 Jan 2026 18:47:41 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/5/GPL/openjdk-27-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='2d85f5a6432abd2eb67b974ed1ab85d2a9557b06be285f2fc6e5d94429951468'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/5/GPL/openjdk-27-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='58f4450fff4f277000cf3d520a612275b0d9b6cb24e1287457d4651e98714b4a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 20 Jan 2026 18:47:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:29:32 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54694fd53c4e9bf4539655dc2b3285316d7e10f220d35530e8e15fe69525013`  
		Last Modified: Tue, 20 Jan 2026 19:21:40 GMT  
		Size: 38.7 MB (38697975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48790a6f53d4070c040a390a332e97a6ea469bf5389ebbc4bf206a2b7d9a3f8`  
		Last Modified: Tue, 20 Jan 2026 18:48:07 GMT  
		Size: 226.0 MB (225999522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:4522cd89bc67e9d4068dc40b993a7771c290d532ed0a145e1ba87989ebdc7719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c546145b606ee5dda7f8dae53d36f6c909a4019d3bd508eedb5ee97420a092`

```dockerfile
```

-	Layers:
	-	`sha256:ee3396d12ff707554c774b0ec169a48486bcd8124484e167dc1aa4ce7372b471`  
		Last Modified: Tue, 20 Jan 2026 19:25:53 GMT  
		Size: 3.7 MB (3653045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:812a642d61120ce61f5148dc751a78fa0c2bbcddb5ee9ba17e3105b2f0920b2d`  
		Last Modified: Tue, 20 Jan 2026 19:25:54 GMT  
		Size: 18.0 KB (18029 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk` - windows version 10.0.26100.32230; amd64

```console
$ docker pull openjdk@sha256:abcb36b51d04b6571e9c56bfa42c5e4594f5f5a770ff5fbfc3bc10f55fdb6d30
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1721044983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d02002222aa11bed971aa6b711f9fe66b1e736021d0df5887a9668eeab2a6af`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 20 Jan 2026 18:51:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 20 Jan 2026 18:51:59 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 20 Jan 2026 18:52:00 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 20 Jan 2026 18:52:06 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 20 Jan 2026 18:52:07 GMT
ENV JAVA_VERSION=27-ea+5
# Tue, 20 Jan 2026 18:52:08 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/5/GPL/openjdk-27-ea+5_windows-x64_bin.zip
# Tue, 20 Jan 2026 18:52:09 GMT
ENV JAVA_SHA256=350ca51cd4321274f6557de42448fd4fc6e845cfe0695800868857f13f89a2fc
# Tue, 20 Jan 2026 18:52:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 20 Jan 2026 18:52:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e72e4b6e32077245586401d96dcbe5dfbfc76b2346166f48cdcfa0df93664650`  
		Last Modified: Tue, 20 Jan 2026 18:52:45 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662149f580d6da5f5f5954a737745aa3ec95b0e3b53799353b7da0257fd4a467`  
		Last Modified: Wed, 21 Jan 2026 06:24:38 GMT  
		Size: 403.4 KB (403418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46759ad4730fb651350be3a6af1de57ca13252b75fb154da903a6887b4a44ff`  
		Last Modified: Tue, 20 Jan 2026 18:52:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843be8db1e5bd4fba522492479b13fb0d3a1fd4bdabd1dea8d4c85ce8481c74e`  
		Last Modified: Tue, 20 Jan 2026 19:01:40 GMT  
		Size: 388.6 KB (388563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a2ea9fbd7e89bcdafe59e0fea26fec21cd3b2776079541fc936fa20a89a547`  
		Last Modified: Tue, 20 Jan 2026 21:05:28 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d009c75f850597872b10e10fa558a19241c9906960ee9d46b8761280f0c82f83`  
		Last Modified: Tue, 20 Jan 2026 18:52:43 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffde2380cd4e2a2a84fed9cab589e7ff1aef81e6b2643b5e9ff3988ad65f20b`  
		Last Modified: Tue, 20 Jan 2026 19:26:24 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465155860de126dae51438501c5c5846510546dd52a805ca574cbcc72c6d48c2`  
		Last Modified: Tue, 20 Jan 2026 18:53:00 GMT  
		Size: 224.5 MB (224484872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e494abfcc7bbb7bc54757d0f4b6c94dbe340549658e352c24a3425cea7e8aa24`  
		Last Modified: Tue, 20 Jan 2026 18:52:43 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-jdk` - windows version 10.0.20348.4648; amd64

```console
$ docker pull openjdk@sha256:36f4ca3dbb5838e1bd200eee72c5ea9460157364de3edd95a48ffcb466c77a3d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2061004440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:983bb2d518ed2afd1c8e299edd57e7849f0b69231b79c051bc6f14b818c56a35`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 20 Jan 2026 18:54:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 20 Jan 2026 18:55:58 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 20 Jan 2026 18:55:59 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 20 Jan 2026 18:56:06 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 20 Jan 2026 18:56:07 GMT
ENV JAVA_VERSION=27-ea+5
# Tue, 20 Jan 2026 18:56:08 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/5/GPL/openjdk-27-ea+5_windows-x64_bin.zip
# Tue, 20 Jan 2026 18:56:10 GMT
ENV JAVA_SHA256=350ca51cd4321274f6557de42448fd4fc6e845cfe0695800868857f13f89a2fc
# Tue, 20 Jan 2026 18:56:44 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 20 Jan 2026 18:56:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:28:58 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12503e819e94357068d715ad8ecf83f339bd5889b12d224bfd56b14fc18ed03`  
		Last Modified: Tue, 20 Jan 2026 18:56:52 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3734874d8df4d7d771d6b1069ee7161637b1c85f22f98b4159d6b88d52986f32`  
		Last Modified: Tue, 20 Jan 2026 19:07:44 GMT  
		Size: 513.0 KB (512968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a40ed685c42672d72a2ca56606735d97bbb3e73fb3efffd84f5dc98f83175c`  
		Last Modified: Tue, 20 Jan 2026 19:07:45 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d298107636bc92dd10715ab2e90da677425c7ef68a7ee07eb9ca510adf2958`  
		Last Modified: Tue, 20 Jan 2026 18:56:52 GMT  
		Size: 360.2 KB (360169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286b4060bec13e685f9eabab1eb4aac12f72419b9a03cc08e06d8721eca263e9`  
		Last Modified: Tue, 20 Jan 2026 19:07:44 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a2735f865a5901c5e0d56b5c640cca88ed7a07e5be27a93ff7cf9dd6362b91`  
		Last Modified: Tue, 20 Jan 2026 19:10:10 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf5658709f37c40a3845d61f68860c77c7d902a98f5c2909661d2568c4b3f58`  
		Last Modified: Tue, 20 Jan 2026 18:56:51 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21bd7fe4f4bae5fc8e5338fddc1e340eadb8313fbb3e3038c89d4e544e288765`  
		Last Modified: Tue, 20 Jan 2026 18:57:06 GMT  
		Size: 224.5 MB (224464285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6cecd6b7b9ff1f44fcab2283976b2e06e2c9218eb6f1e613530da7e757264b`  
		Last Modified: Tue, 20 Jan 2026 18:56:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
