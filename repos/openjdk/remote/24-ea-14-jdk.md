## `openjdk:24-ea-14-jdk`

```console
$ docker pull openjdk@sha256:e405f382677a7fe0a3d41c4538d0e1c78828a74cff16f68f434b7109f79031e3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `openjdk:24-ea-14-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:b159ded0cf121c02fd216f9037a1c9175c7c11af45b5552e87d089de20175a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301489577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c6db179c05511cd99f61dba6ced7ca2ab8bea8626a013c4f7d6e0121b52cfdb`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 06 Sep 2024 18:48:13 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 06 Sep 2024 18:48:13 GMT
CMD ["/bin/bash"]
# Fri, 06 Sep 2024 18:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 06 Sep 2024 18:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 06 Sep 2024 18:48:13 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 18:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 06 Sep 2024 18:48:13 GMT
ENV JAVA_VERSION=24-ea+14
# Fri, 06 Sep 2024 18:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/14/GPL/openjdk-24-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='e3cf94d73e0ca63c536e901858cb97a0053c62606f8bb9d5b2ca20e1cc573d0c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/14/GPL/openjdk-24-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='0d13500ae2e96601c70e90fca2ad928c3bf541afc71c293aed33924a2361d97a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 06 Sep 2024 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5e407bf3af905fb1f6edf271f870052697e79b018f921119921615cd25365fdb`  
		Last Modified: Tue, 10 Sep 2024 01:02:42 GMT  
		Size: 49.2 MB (49239252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a87f9d67e2d21e2798c86432dad12f7f48ed183498d0975b68916bc4102c1a`  
		Last Modified: Tue, 10 Sep 2024 01:54:50 GMT  
		Size: 40.4 MB (40418113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9285c8120b81c73c125c64f3a20e9459f1cd26ed2dc6b7f5cbee8c6e994e91`  
		Last Modified: Tue, 10 Sep 2024 01:54:52 GMT  
		Size: 211.8 MB (211832212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-14-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:260ac5795c0020d08bf40ce793e13fcd12e28fdb25272dac38f9a2bab029f3a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3690210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac388db3710a73a9541725631bb7baecbf4019716e3cd2c4d4f70714458fcb3`

```dockerfile
```

-	Layers:
	-	`sha256:6804131feb910f8b3cf8f6d2af1529778b3ee6b4ab6625bd4077021a066adef1`  
		Last Modified: Tue, 10 Sep 2024 01:54:49 GMT  
		Size: 3.7 MB (3670499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b5d8c3c243cea077a1f9f1baa8d2f6aa88f43f52be2d47206e016edbd69d20f`  
		Last Modified: Tue, 10 Sep 2024 01:54:49 GMT  
		Size: 19.7 KB (19711 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-14-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2aee2e344f25c64f610492f3bb0570e3535246eb5689c3ce29771854b2a8be4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298440742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df4746cecdcf50e5d091cb52bda3efcd9e1fee19d1b7d68100e4f5bdca773db`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 06 Sep 2024 18:48:13 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 06 Sep 2024 18:48:13 GMT
CMD ["/bin/bash"]
# Fri, 06 Sep 2024 18:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 06 Sep 2024 18:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 06 Sep 2024 18:48:13 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 18:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 06 Sep 2024 18:48:13 GMT
ENV JAVA_VERSION=24-ea+14
# Fri, 06 Sep 2024 18:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/14/GPL/openjdk-24-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='e3cf94d73e0ca63c536e901858cb97a0053c62606f8bb9d5b2ca20e1cc573d0c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/14/GPL/openjdk-24-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='0d13500ae2e96601c70e90fca2ad928c3bf541afc71c293aed33924a2361d97a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 06 Sep 2024 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ed6a7145c00ee1c4b91b6b37765e2a7addef2d9b96e12546b2f7aad0a198ae3f`  
		Last Modified: Tue, 10 Sep 2024 05:32:56 GMT  
		Size: 47.9 MB (47913808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb8c247ecf1b88686d212c2f55e0f5ac4d4ba8cde9b5d6f216ca338a07e7b87`  
		Last Modified: Tue, 10 Sep 2024 06:43:07 GMT  
		Size: 40.8 MB (40844369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a72a008ebaa9bb3ede37884b879b51cf951f85041072ba6452f0c21c29d0b24`  
		Last Modified: Tue, 10 Sep 2024 06:43:11 GMT  
		Size: 209.7 MB (209682565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-14-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:937563d7d466e22eb8fa0a84d5da1ff478f610f7c4cb6730b09ae0e5f2dabce7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3689146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295fb42a8de154fdb8f982b5bbdffe9a03c6efabd167a30c227bbb801c374c7b`

```dockerfile
```

-	Layers:
	-	`sha256:9cab0fbd0e3192c3ae01112bae8f67a80cd4d625056ce1d999a77cc5d08bffda`  
		Last Modified: Tue, 10 Sep 2024 06:43:05 GMT  
		Size: 3.7 MB (3668882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e4d4fe2df8e3d3e022a6e9cd9fc77d8e07e506f1f9ac4d18271a03f498bb56c`  
		Last Modified: Tue, 10 Sep 2024 06:43:05 GMT  
		Size: 20.3 KB (20264 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-14-jdk` - windows version 10.0.20348.2700; amd64

```console
$ docker pull openjdk@sha256:dd27fbf434011feb9ed358fd0e14bc4418ea9673946fcafc0d0277230aa6bc1c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1670880164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45b25899c4a726b5b91fd26737821ea6ebe9e71b81260c69faa96dd9dd281127`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 11 Sep 2024 00:05:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 00:05:45 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:05:46 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 11 Sep 2024 00:05:56 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:05:56 GMT
ENV JAVA_VERSION=24-ea+14
# Wed, 11 Sep 2024 00:05:57 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/14/GPL/openjdk-24-ea+14_windows-x64_bin.zip
# Wed, 11 Sep 2024 00:05:58 GMT
ENV JAVA_SHA256=d302c4d8be4955ea17267c66b8321f205212748df83273e4e0d9ccc0d1c4b1a2
# Wed, 11 Sep 2024 00:06:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:06:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c083dbe4899aa80edc0b3da05d5550f4f6266c39dcaa60cbe6c6efbedda26ea6`  
		Last Modified: Wed, 11 Sep 2024 00:06:36 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1db50d237b35e81f0d6928f3ba8fc54ac920d814cec557b40ebe6c817f144461`  
		Last Modified: Wed, 11 Sep 2024 00:06:36 GMT  
		Size: 350.3 KB (350272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae6fb62d256c807fb5e8cf71226d89e798a131bad7747dc6873af847bf331b0`  
		Last Modified: Wed, 11 Sep 2024 00:06:36 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5da85c27f59e4765def4b8a91d01012e5ae490c6561a23a3d7b285a9b54bbdb`  
		Last Modified: Wed, 11 Sep 2024 00:06:36 GMT  
		Size: 334.4 KB (334384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80eea04ec36e869c78e327a6cb581f645ed5db74ea99e1d2bf20efbf879fb50e`  
		Last Modified: Wed, 11 Sep 2024 00:06:35 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a6eae4fbe508742cfc8cf1c138644e811c573d938b72e274b4ad09145b1e9b`  
		Last Modified: Wed, 11 Sep 2024 00:06:35 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f906f1534fb8e742202030975053d2347538a937e51f6848c1ba7ea1fe74e754`  
		Last Modified: Wed, 11 Sep 2024 00:06:35 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15fe23ef12e2d275172bde28df3cf71d00fd9d1845730f6609d923d5a9daf4f6`  
		Last Modified: Wed, 11 Sep 2024 00:06:46 GMT  
		Size: 208.0 MB (207995190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef47a3d3dda447bb6ebdb64d2ba1b101d8ad6f5bc615598f8640fbec73439d55`  
		Last Modified: Wed, 11 Sep 2024 00:06:35 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-ea-14-jdk` - windows version 10.0.17763.6293; amd64

```console
$ docker pull openjdk@sha256:b6eb09f8c9d15934afd65a0826d8a758baaa1b286a7357d24c29bda324c51bbb
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1928945265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a545230b25cf1a45284d5fa2d0b31b2c4345b2331d0d29fe4b3f3bb8060934`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 00:04:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 00:05:00 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:05:00 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 11 Sep 2024 00:05:10 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:05:10 GMT
ENV JAVA_VERSION=24-ea+14
# Wed, 11 Sep 2024 00:05:11 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/14/GPL/openjdk-24-ea+14_windows-x64_bin.zip
# Wed, 11 Sep 2024 00:05:12 GMT
ENV JAVA_SHA256=d302c4d8be4955ea17267c66b8321f205212748df83273e4e0d9ccc0d1c4b1a2
# Wed, 11 Sep 2024 00:05:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:05:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326c5813accafbcd1f1c0387849f28862d1ea4afd85fb083471f6f94115d18ed`  
		Last Modified: Wed, 11 Sep 2024 00:05:54 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df4033bd2962354ca92def3ab9e0596cf56954c6bf73ff59cf4bfcd8b17454c`  
		Last Modified: Wed, 11 Sep 2024 00:05:55 GMT  
		Size: 343.8 KB (343783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81cae26b9113f0621a70ecb9d1fd6149dc0c0143d733d1089413ece35be8770c`  
		Last Modified: Wed, 11 Sep 2024 00:05:54 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123b176758bf7a7f5577c2a50fe31d7d78fcc512ad18594f4f272917c714bc9b`  
		Last Modified: Wed, 11 Sep 2024 00:05:55 GMT  
		Size: 330.1 KB (330092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36beb21a7e22624e0e793aa13e5e91303b4db8787c2afc9a6867c10db8e47083`  
		Last Modified: Wed, 11 Sep 2024 00:05:53 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f8261675c8fabc36e464c0aa83d5f1917c18d617046c82e59775e4a65637c5c`  
		Last Modified: Wed, 11 Sep 2024 00:05:53 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6b072c3c62285b2fa0f9382eb32cb3a901473ccd723f52da14aab4141fbd91`  
		Last Modified: Wed, 11 Sep 2024 00:05:53 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff351f71740d0c2fff83f4c2eb26079e7756ab58d58348fa7e424806303de84`  
		Last Modified: Wed, 11 Sep 2024 00:06:04 GMT  
		Size: 208.0 MB (207995284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9b1a2c6dccf1bc0323e2f2b25d0f3bf4eaa55552a7848f808dd64e32b21753`  
		Last Modified: Wed, 11 Sep 2024 00:05:53 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
