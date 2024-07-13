## `openjdk:23-ea-jdk`

```console
$ docker pull openjdk@sha256:f6bf12c6b81ad3355de7fb6631e15e076af20418cccdb3f17d35d3f9e6d62ea7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.20348.2582; amd64
	-	windows version 10.0.17763.6054; amd64

### `openjdk:23-ea-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:42402bd0c9431aadf2a000c8c9273ca12f716d7b0a0f66d860b0066a49123139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.2 MB (298171895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bcef58001bb334b8b57224f43df6cf29e935c3dc4b1fc303aa7a87cd25f878b`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
CMD ["/bin/bash"]
# Fri, 12 Jul 2024 06:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 12 Jul 2024 06:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 12 Jul 2024 06:48:10 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 06:48:10 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jul 2024 06:48:10 GMT
ENV JAVA_VERSION=23-ea+31
# Fri, 12 Jul 2024 06:48:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/31/GPL/openjdk-23-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='49af9ea82c1a9396a8c8529334d26ec7c835b217c790965708fbdbf29fb46ba2'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/31/GPL/openjdk-23-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='2bde94ea8c9261ad53a1644b2e04cb13a6ab4c95d2649beff2cbd6f176b8465d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jul 2024 06:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c77822463f50dcf3516376e15ec30057a89604a1a2eab9873d521f343c1180b`  
		Last Modified: Fri, 12 Jul 2024 21:57:24 GMT  
		Size: 37.9 MB (37872153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06af5af9eee62452221f2f29a3a817cf9ba961c46205fa9dfff4c510ecec607`  
		Last Modified: Fri, 12 Jul 2024 21:57:28 GMT  
		Size: 211.3 MB (211306006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:335a7c5df1000f04a42a61ab96a08534e38b7dd3e268668fc0b2a7e13a71137c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3352772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:950dc04881855b6fe91f815af2c9b6ee2abd4165a7d037db9e5f81df41921c81`

```dockerfile
```

-	Layers:
	-	`sha256:f564b0e47abcc7cfb111098b207ac23f16d07ed4ed66924fce547cd5c35a0235`  
		Last Modified: Fri, 12 Jul 2024 21:57:24 GMT  
		Size: 3.3 MB (3333244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1775e1518bc231842c0d8c1290bbc85e7bdc5ed4139ca7e6521e27a7cbc4a177`  
		Last Modified: Fri, 12 Jul 2024 21:57:24 GMT  
		Size: 19.5 KB (19528 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e8c0d537fdc7c4ca0599947a5f9fa62ec54190b0e7cdcd4a81a805189fc8f6d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295094478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c166b9ea98370605d7ed314484374461bcb300a15db12c6d4565d00e19ba7980`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Jul 2024 22:40:25 GMT
ADD file:a5d614a69430ac76660689e833533429bd70568280b25af98af60b01a76d6139 in / 
# Mon, 08 Jul 2024 22:40:26 GMT
CMD ["/bin/bash"]
# Fri, 12 Jul 2024 06:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 12 Jul 2024 06:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 12 Jul 2024 06:48:10 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 06:48:10 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jul 2024 06:48:10 GMT
ENV JAVA_VERSION=23-ea+31
# Fri, 12 Jul 2024 06:48:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/31/GPL/openjdk-23-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='49af9ea82c1a9396a8c8529334d26ec7c835b217c790965708fbdbf29fb46ba2'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/31/GPL/openjdk-23-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='2bde94ea8c9261ad53a1644b2e04cb13a6ab4c95d2649beff2cbd6f176b8465d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jul 2024 06:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c72f53f7235bf26fdb27eaeb0d712fc1886f19eda2722ef9709dda7424814b9e`  
		Last Modified: Mon, 08 Jul 2024 22:41:23 GMT  
		Size: 47.7 MB (47652661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3129baf21359e4eb83f9d1391c216edfe6dce92354dbd70df14232415144a124`  
		Last Modified: Fri, 12 Jul 2024 22:04:48 GMT  
		Size: 38.3 MB (38259249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9a00d939815c50426c216f154aff6fd9aef7c065f90a37f68c3574784f5b3c`  
		Last Modified: Fri, 12 Jul 2024 22:10:35 GMT  
		Size: 209.2 MB (209182568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:f9d564c63c104474b22514df2968b4077bde92d7011a962ce73e4a7f962f104c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3351630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5918d729433ebdef04e83b0ed14f7fcf18a3b37ffc2bef6bc8598f067b432cc`

```dockerfile
```

-	Layers:
	-	`sha256:cfed7b8049daed2ced7b8459df3d69f668013ec86610e8f6f08c0ecdeea2700e`  
		Last Modified: Fri, 12 Jul 2024 22:10:30 GMT  
		Size: 3.3 MB (3331627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf095faccb79c0798369fb4505364eef0f1d151baf152400b3f5590fb7d6d221`  
		Last Modified: Fri, 12 Jul 2024 22:10:30 GMT  
		Size: 20.0 KB (20003 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-jdk` - windows version 10.0.20348.2582; amd64

```console
$ docker pull openjdk@sha256:83de0e5da6c2e07e8768e135fc551c7f91f7cb42106a6d5bf04e6f4882ed3060
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346749993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16123944cec3a5879ce76788de77f5f6cdb2cdf1e4cf2c07ae2dd071ae9dd3cb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Fri, 12 Jul 2024 22:00:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 12 Jul 2024 22:01:05 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 12 Jul 2024 22:01:06 GMT
ENV JAVA_HOME=C:\openjdk-23
# Fri, 12 Jul 2024 22:01:12 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 12 Jul 2024 22:01:12 GMT
ENV JAVA_VERSION=23-ea+31
# Fri, 12 Jul 2024 22:01:13 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/31/GPL/openjdk-23-ea+31_windows-x64_bin.zip
# Fri, 12 Jul 2024 22:01:14 GMT
ENV JAVA_SHA256=7894a87e50c30dfa4be1f1432dfb289c4de40e1c0fd447b8f4b5fce3141e6615
# Fri, 12 Jul 2024 22:01:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 12 Jul 2024 22:01:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0206d135152eb909f50159d6ca348a5aead199afacbafc000b770c1b0720f6`  
		Last Modified: Tue, 09 Jul 2024 18:30:31 GMT  
		Size: 751.0 MB (751001543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18a50da7446f6b879900d4a46641e38ebbddc6006b94f71a2f3237c06d89acfa`  
		Last Modified: Fri, 12 Jul 2024 22:01:40 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f65a5bf071f393dbfa3d42014a3d3142bb76c0035b57fd311b94132edd15a0fa`  
		Last Modified: Fri, 12 Jul 2024 22:01:40 GMT  
		Size: 359.6 KB (359587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18dd96e949fcaf81c98afa509c043c4cc04aca6ffc122586f646de13b5cf02b4`  
		Last Modified: Fri, 12 Jul 2024 22:01:39 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c27130019b0d98ed213425d82413a23238997d405a0607e2f429d5e408f9d6d1`  
		Last Modified: Fri, 12 Jul 2024 22:01:40 GMT  
		Size: 346.1 KB (346144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c40013168fbbb7e81331173e0eb945c1867227485ca56ff26e36c46e72330a`  
		Last Modified: Fri, 12 Jul 2024 22:01:38 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0bd54db4c1ebe2aafd17c57a9d2cc352884132d6b4e2618f09c0c314647857`  
		Last Modified: Fri, 12 Jul 2024 22:01:37 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29a248220857a340bd6df7ea494655fca068a4679f8761680a1177f05b520e6d`  
		Last Modified: Fri, 12 Jul 2024 22:01:38 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea9a3f678d7a2cd9120cefa308f1f5d8b48788deea8fb2c284d39f43c634937`  
		Last Modified: Fri, 12 Jul 2024 22:01:49 GMT  
		Size: 206.4 MB (206436219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f38cfc8c3a631f2de1186966ae41ac1f938880ee40de66a860253c2ae5b146c3`  
		Last Modified: Fri, 12 Jul 2024 22:01:38 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:23-ea-jdk` - windows version 10.0.17763.6054; amd64

```console
$ docker pull openjdk@sha256:3610b7fea5f423b9172d83a8ca638462d58e5f1d72e0662ca95c601ddca33b00
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2445733678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:323f9a364646f0f49617668117e43a9444200f938b18526177ac02263b9a87f7`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Fri, 12 Jul 2024 22:07:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 12 Jul 2024 22:08:23 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 12 Jul 2024 22:08:24 GMT
ENV JAVA_HOME=C:\openjdk-23
# Fri, 12 Jul 2024 22:08:44 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 12 Jul 2024 22:08:45 GMT
ENV JAVA_VERSION=23-ea+31
# Fri, 12 Jul 2024 22:08:46 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/31/GPL/openjdk-23-ea+31_windows-x64_bin.zip
# Fri, 12 Jul 2024 22:08:46 GMT
ENV JAVA_SHA256=7894a87e50c30dfa4be1f1432dfb289c4de40e1c0fd447b8f4b5fce3141e6615
# Fri, 12 Jul 2024 22:09:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 12 Jul 2024 22:09:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e038a148c7feb7f6010c1a044eab9010d7366ab1fb7354bf3b1c47a5a899c5`  
		Last Modified: Fri, 12 Jul 2024 22:09:32 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5a09613aba4fe06f7a33a4835642da64c9046a3ba825deaf232d6ff53ebd87f`  
		Last Modified: Fri, 12 Jul 2024 22:09:33 GMT  
		Size: 499.5 KB (499451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c636eb003f485953497b0c84c27688c71b18f764c6609c1546aabeff7347395`  
		Last Modified: Fri, 12 Jul 2024 22:09:32 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:181510fa1de9a60c846800436a088f4d2cb5934c9175973eaa381e31122d28c8`  
		Last Modified: Fri, 12 Jul 2024 22:09:32 GMT  
		Size: 351.3 KB (351272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423b6a3d8d9b45b5894ac877a42feccabc49fbf7ed8ce3bab9864501e9a182e0`  
		Last Modified: Fri, 12 Jul 2024 22:09:30 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44444c0cd7387445289886fb4133a979f4cd09dd206dc4b2b7af4ff966ed64c`  
		Last Modified: Fri, 12 Jul 2024 22:09:30 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2291c13bd05a63826b47b0ee530a041dccf8f00fc1bbbcf3f077a45b83e5c37a`  
		Last Modified: Fri, 12 Jul 2024 22:09:30 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71d5824591b9663c45a15dc762c052a8e43d1fe7365b96439431495da924a9f`  
		Last Modified: Fri, 12 Jul 2024 22:09:41 GMT  
		Size: 206.4 MB (206445751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35fd2491ff21be1bde2b47a997dcbde2488df01ebea2aaa7771668517d82b08c`  
		Last Modified: Fri, 12 Jul 2024 22:09:30 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
