## `openjdk:27-ea-22-jdk`

```console
$ docker pull openjdk@sha256:d4f73cd35df4cc034d5178ff56e785e30dc18a7daeda979fb7a2a051a51e03ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `openjdk:27-ea-22-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:15b38b210402e3de2f629029f1862611aa80c40410bfd278357c969799e2e215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.6 MB (309574667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4190ab05ae216f5b9aa05e6775f2a86e8ffd8911b47ef12af276ca13ad7c7f2`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:44:08 GMT
ADD oraclelinux-10-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:08 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 20:18:26 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 15 May 2026 20:18:39 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Fri, 15 May 2026 20:18:39 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:18:39 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2026 20:18:39 GMT
ENV JAVA_VERSION=27-ea+22
# Fri, 15 May 2026 20:18:39 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/22/GPL/openjdk-27-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='47b58a37806dcaf954eb174f682514b06f17b8205d154ad84c2f68666c302570'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/22/GPL/openjdk-27-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='87c706c502d3fa5d8a8ff7bf543c7903207fb8d5a11ed637fe05ed33b8179702'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 May 2026 20:18:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ded2aa0abafd1e1e93e05338cb1b14916dbeb283d3862aa21e5d8b0164f4cbf3`  
		Last Modified: Tue, 12 May 2026 18:44:20 GMT  
		Size: 43.1 MB (43080582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846ebf29aec2dec2e17e26d8c2c7669305e946fb12da2410c3089793aeb38196`  
		Last Modified: Fri, 15 May 2026 20:19:01 GMT  
		Size: 37.7 MB (37687895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b99930b49e490efad118f74bd9ad8d36f25982bec8fac52b508ae5de2dad10d`  
		Last Modified: Fri, 15 May 2026 20:19:05 GMT  
		Size: 228.8 MB (228806190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-22-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:9f24d387ba46f03ef53460f14577240518cc604f467a0ae63dce1abbada35baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c5de8f7eb291535c50a97fa30a7ac992160a6067ec73027d8f9d8c9f3fb943`

```dockerfile
```

-	Layers:
	-	`sha256:a7e34bc63a6b8b54834ad94bb801902126683d8a9f7ecf7d1bb0ce5d58f97486`  
		Last Modified: Fri, 15 May 2026 20:18:59 GMT  
		Size: 2.4 MB (2367743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c20f59eac3ec7e40b94635381f278fbd39c25ab4d08d4d9bede84a7a4a23e9c1`  
		Last Modified: Fri, 15 May 2026 20:18:59 GMT  
		Size: 17.8 KB (17848 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-22-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:286ea803910a21946f30839f5a4f9ee9c86fad2773bf59073a0d74494f9b6e31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.0 MB (305960720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a6b129c0701c2d72aae2480c47050113f51d274d515163415383f8f44c1d7a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:43:55 GMT
ADD oraclelinux-10-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:43:55 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 20:18:09 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 15 May 2026 20:18:23 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Fri, 15 May 2026 20:18:23 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:18:23 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2026 20:18:23 GMT
ENV JAVA_VERSION=27-ea+22
# Fri, 15 May 2026 20:18:23 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/22/GPL/openjdk-27-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='47b58a37806dcaf954eb174f682514b06f17b8205d154ad84c2f68666c302570'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/22/GPL/openjdk-27-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='87c706c502d3fa5d8a8ff7bf543c7903207fb8d5a11ed637fe05ed33b8179702'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 May 2026 20:18:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:523b5fcd95921b1880258a8c56e30985e8f3adf21d143bf177907dc76d6a562b`  
		Last Modified: Tue, 12 May 2026 18:44:06 GMT  
		Size: 41.5 MB (41495695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211bee5ff420ccd7d1e415cecdf86fb1ca49a2aed221aec6cb952520b42cab2a`  
		Last Modified: Fri, 15 May 2026 20:18:47 GMT  
		Size: 37.7 MB (37701706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9b3cabe86e6f5dfb87dac4208ac2d6704fa8324cb61a8a042159f0d1c9ed71`  
		Last Modified: Fri, 15 May 2026 20:18:53 GMT  
		Size: 226.8 MB (226763319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-22-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:f1ad0838554683df68f560cffd810ff83ae9fdd0874ce012a2390a9f86716506
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86a63b9a1771a1991a40008fd36c0a740ad617b704e631f4f3e2007e16e4a30`

```dockerfile
```

-	Layers:
	-	`sha256:8bd64f1ba2ea2ea031a203af12f036ebca4776207e0fb07d091e54826a6236cd`  
		Last Modified: Fri, 15 May 2026 20:18:44 GMT  
		Size: 2.4 MB (2367271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc176cce0b08aa7dcc86ab9db0ee931303b0fae1140f099f1fdc1db5707d3f89`  
		Last Modified: Fri, 15 May 2026 20:18:45 GMT  
		Size: 18.1 KB (18065 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-22-jdk` - windows version 10.0.26100.32860; amd64

```console
$ docker pull openjdk@sha256:35d6e71f7f1e802461342b476c01e408cdcd57f85ae2c1ab06c298d340189096
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2431968714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:979df0baff7a1516dfda4ba1ce6b9f3abe410e55abd2599128c231859113d837`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Fri, 15 May 2026 21:10:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 15 May 2026 21:11:02 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 15 May 2026 21:11:04 GMT
ENV JAVA_HOME=C:\openjdk-27
# Fri, 15 May 2026 21:11:11 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 15 May 2026 21:11:12 GMT
ENV JAVA_VERSION=27-ea+22
# Fri, 15 May 2026 21:11:12 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/22/GPL/openjdk-27-ea+22_windows-x64_bin.zip
# Fri, 15 May 2026 21:11:13 GMT
ENV JAVA_SHA256=8f070229867cab472c5d736b8a2b08d610772c4da7d6e451ab494e77fa4ad88d
# Fri, 15 May 2026 21:12:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 15 May 2026 21:12:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:915521ee20f379f50a06d4f22330e0f6b880411357921aceff959d4549c62fde`  
		Last Modified: Fri, 15 May 2026 21:12:35 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b6e349719dd85cb482ff567e3d7f785bd84849f2f198dcccdef658a6ea4a75`  
		Last Modified: Fri, 15 May 2026 21:12:35 GMT  
		Size: 361.3 KB (361283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e234040c4048269a05c53ee25ef9fe75bd01c137abc58fe06ca1c2c38b0ebc9`  
		Last Modified: Fri, 15 May 2026 21:12:35 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c07fa7d71a965015cc4bab16430f7f83f750021fd7430d375b789ef12933eb0`  
		Last Modified: Fri, 15 May 2026 21:12:35 GMT  
		Size: 347.5 KB (347533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8663b0d39c4e9b37542a978d9e84b650b99265e844731522289077af6d3d0a6d`  
		Last Modified: Fri, 15 May 2026 21:12:33 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b334f34deab3ec5a5c347a95ad24c15e31c0583d3ddf19f8015361de5ff80b`  
		Last Modified: Fri, 15 May 2026 21:12:33 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acb8bcd1d3f468ec6541749ea988cd0ca9e28d2899e3ee3db2622b8433fa67c0`  
		Last Modified: Fri, 15 May 2026 21:12:33 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a79705a2c75733b509f4c4bb49814b29351dd347c0795ebcf7004a4419449d80`  
		Last Modified: Fri, 15 May 2026 21:12:48 GMT  
		Size: 225.3 MB (225310301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c3f8635e9146f0a176a18d7d34d35a294c0ec6ac451df0a9c1fb28875699f80`  
		Last Modified: Fri, 15 May 2026 21:12:33 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-22-jdk` - windows version 10.0.20348.5139; amd64

```console
$ docker pull openjdk@sha256:2735f40ba892a7a2014bcc81e76b8fe573ce21786455220513132ee343f95bfd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2348641977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67be72b2b6578087cfb3b90777f8d4c86d9a7ae45931b65cc79db2026e7482f8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Fri, 15 May 2026 20:39:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 15 May 2026 20:40:31 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 15 May 2026 20:40:32 GMT
ENV JAVA_HOME=C:\openjdk-27
# Fri, 15 May 2026 20:40:39 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 15 May 2026 20:40:40 GMT
ENV JAVA_VERSION=27-ea+22
# Fri, 15 May 2026 20:40:40 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/22/GPL/openjdk-27-ea+22_windows-x64_bin.zip
# Fri, 15 May 2026 20:40:42 GMT
ENV JAVA_SHA256=8f070229867cab472c5d736b8a2b08d610772c4da7d6e451ab494e77fa4ad88d
# Fri, 15 May 2026 20:41:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 15 May 2026 20:41:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd4acf5065d2387bdf6560dbeefafc544ff9e00260a8c40d1631cff4a5aeb93`  
		Last Modified: Fri, 15 May 2026 20:41:20 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc9293fa70683c115ba9e34ce61cf8c47d413582df71dfcdd0e53966c44394d`  
		Last Modified: Fri, 15 May 2026 20:41:20 GMT  
		Size: 516.2 KB (516199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f5ae04cad74d2cdd49ae2d2d256fa443edb4d71ac801358bbc4e38280ba279`  
		Last Modified: Fri, 15 May 2026 20:41:20 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0afc5d026b3a384322069086353d1e15be1ddbad62e746d6b19d8327f144ff7b`  
		Last Modified: Fri, 15 May 2026 20:41:20 GMT  
		Size: 361.0 KB (360965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a581af4b07befb8bdade24c47ae4e97f09e31588192cc943f7e3912081d26f`  
		Last Modified: Fri, 15 May 2026 20:41:18 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0585e87d942475b8c7b05f2a023ce00420bc93feb5ffa03cdfc468509726cd31`  
		Last Modified: Fri, 15 May 2026 20:41:18 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2b54c1752d87e27efcf942a04b050b34101260cd8461f05ae849e2a23f7ba2`  
		Last Modified: Fri, 15 May 2026 20:41:18 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb1221a40f1929cc57d113ca48c54589c17b84bd6b9b192dc75479f70ef7631`  
		Last Modified: Fri, 15 May 2026 20:41:34 GMT  
		Size: 225.3 MB (225336334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779c0dffd3e971ac310fad82726e92890b9e9fd3d75cdc43ddf6583f08dd73a5`  
		Last Modified: Fri, 15 May 2026 20:41:18 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
