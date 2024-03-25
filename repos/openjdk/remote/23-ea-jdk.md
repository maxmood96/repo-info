## `openjdk:23-ea-jdk`

```console
$ docker pull openjdk@sha256:362c19bc600b20e00bbc1fb5b056c5ae0bf4345eeac3490f73c07390888df4ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.20348.2340; amd64
	-	windows version 10.0.17763.5576; amd64

### `openjdk:23-ea-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:79163db329c780a8c8f37f84c6235dda02f3356825fd08dc88d91544f96898cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.5 MB (289476999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5369da73efdcc05eb015464f6c53e592e71088f3c9333b163729284251b1b837`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:04 GMT
ADD file:9bcef05fa351e2fb72a4b6052a0252eeaa2cff794ed089a482670c67961d2e90 in / 
# Fri, 08 Mar 2024 19:21:04 GMT
CMD ["/bin/bash"]
# Fri, 15 Mar 2024 16:08:04 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 15 Mar 2024 16:08:04 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 15 Mar 2024 16:08:04 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 16:08:04 GMT
ENV LANG=C.UTF-8
# Fri, 15 Mar 2024 16:08:04 GMT
ENV JAVA_VERSION=23-ea+14
# Fri, 15 Mar 2024 16:08:04 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/14/GPL/openjdk-23-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='9305399006d6c477d1c84cc48d42d44839199f603c1802298225c13160f1d9d2'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/14/GPL/openjdk-23-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='7eb97e59d151dbd147eb589d4de888a522e5f5ec8688a65465ecc8ddee5a0f84'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Mar 2024 16:08:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:972029ff9873af36c6c0fcee05b14acbc57a61ecd0b8bf86b167bdf46f973823`  
		Last Modified: Fri, 08 Mar 2024 19:22:31 GMT  
		Size: 49.0 MB (48978454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7bf66d4984a0af52297b870b1bec7972ac9dae49ffaafb2d48cc862e4b18948`  
		Last Modified: Fri, 15 Mar 2024 23:55:57 GMT  
		Size: 37.7 MB (37733350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25254ac94875805b7f08940e29ec52c17cc60b668e0879ed43a8074f7ea2ea79`  
		Last Modified: Fri, 15 Mar 2024 23:56:00 GMT  
		Size: 202.8 MB (202765195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:e0db65ea6d1e1330440dbb4b6919ec7619bbb16a182eb130ae7cf6ed055e0f00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3349411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b26e47c9e59021bec6683da8898b2e150dfbab19580a5b75e136c6a8c12af63`

```dockerfile
```

-	Layers:
	-	`sha256:2e7be5e179b99f955cce7a918f7f5bbe16736986a1e44da4b76915e1023f560f`  
		Last Modified: Fri, 15 Mar 2024 23:55:56 GMT  
		Size: 3.3 MB (3329522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1979087ab30f36a5923628862c40b996607e6faaef54e3dc84146d930fb2dc19`  
		Last Modified: Fri, 15 Mar 2024 23:55:56 GMT  
		Size: 19.9 KB (19889 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:3463083d7a54bb57200a2d16c15eb87c4f729c8e09cde2942273b88530905643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.4 MB (286428309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cffeddc4e5000f8ad0298c5bc019f9b9f23edbdb241783db7adffc76a215dce3`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 08 Mar 2024 19:48:53 GMT
ADD file:71724b501850c3e6cd72efc58b3430394f691a428c2c62755eac0b93c5579f35 in / 
# Fri, 08 Mar 2024 19:48:53 GMT
CMD ["/bin/bash"]
# Fri, 15 Mar 2024 16:08:04 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 15 Mar 2024 16:08:04 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 15 Mar 2024 16:08:04 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 16:08:04 GMT
ENV LANG=C.UTF-8
# Fri, 15 Mar 2024 16:08:04 GMT
ENV JAVA_VERSION=23-ea+14
# Fri, 15 Mar 2024 16:08:04 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/14/GPL/openjdk-23-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='9305399006d6c477d1c84cc48d42d44839199f603c1802298225c13160f1d9d2'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/14/GPL/openjdk-23-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='7eb97e59d151dbd147eb589d4de888a522e5f5ec8688a65465ecc8ddee5a0f84'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Mar 2024 16:08:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5c53b3bc8702e4b172b3fdde99731082a493b5f5fdd7e9632b3cf7dea02a52b4`  
		Last Modified: Fri, 08 Mar 2024 19:49:57 GMT  
		Size: 47.7 MB (47664888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71597242e3bc84850918d978b72bcf84c5867bfb6441051c67b805dca13e66a`  
		Last Modified: Sat, 16 Mar 2024 15:50:44 GMT  
		Size: 38.1 MB (38140694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f0647b5a01cfcf58d84174f7b6488e248162cd2e4d60fe0994ec193a89ba2c`  
		Last Modified: Sat, 16 Mar 2024 15:50:48 GMT  
		Size: 200.6 MB (200622727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:ab705c5bd9ecb2128dcd68ed46c6db9f02f654a8b24792dee17ec6ab0b461cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3346687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb20d6ac7a4e8ee685070a716f3f6632285b07344bec5a357cc19aec40317bf7`

```dockerfile
```

-	Layers:
	-	`sha256:2069872da5b4d1f97d55f9316c39cc372a87ad96d863333a624583e128008ab1`  
		Last Modified: Sat, 16 Mar 2024 15:50:43 GMT  
		Size: 3.3 MB (3326760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67d300e28e93fdeffcca2d0b1ecc74c0036328ebaef94f5edef7de193162f37d`  
		Last Modified: Sat, 16 Mar 2024 15:50:42 GMT  
		Size: 19.9 KB (19927 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-jdk` - windows version 10.0.20348.2340; amd64

```console
$ docker pull openjdk@sha256:ee2378888fd65cc1cb3ffaf41a923a5684f0f7d29e8538407223f8bc1107504b
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2155864289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e2ab62d0e85e3bad3fae5cd3a334781dceaec468f5151be3f82e15ab9fbecb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Mon, 25 Mar 2024 19:12:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Mar 2024 19:12:55 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 25 Mar 2024 19:12:55 GMT
ENV JAVA_HOME=C:\openjdk-23
# Mon, 25 Mar 2024 19:13:03 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 25 Mar 2024 19:13:04 GMT
ENV JAVA_VERSION=23-ea+15
# Mon, 25 Mar 2024 19:13:04 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/15/GPL/openjdk-23-ea+15_windows-x64_bin.zip
# Mon, 25 Mar 2024 19:13:05 GMT
ENV JAVA_SHA256=990a13730f096e195392211ecd4623c364cae742a9aedb5aae232c629b08f2b6
# Mon, 25 Mar 2024 19:13:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 25 Mar 2024 19:13:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f8557839336a7916e35f38d2bc8ffa6f5cae2c4078eec439dd2ed236bb0264`  
		Last Modified: Mon, 25 Mar 2024 19:13:40 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9caf8f1404b63352316c4b57850e0419f245ba118fb9c45202072a58f231a6e5`  
		Last Modified: Mon, 25 Mar 2024 19:13:40 GMT  
		Size: 505.0 KB (504962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b2162f9d2c138b0479b408efb83767e6c9b42978841d50770732475fa18ab71`  
		Last Modified: Mon, 25 Mar 2024 19:13:39 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26a4d6ba2765f04bbfa84a9778c0395a659260edb41ce7775750855a42d6cf61`  
		Last Modified: Mon, 25 Mar 2024 19:13:39 GMT  
		Size: 345.4 KB (345444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62e46e9e8b6fb401af7fe860134cc17df22b08b6da94a6541fc0cbe315de08c1`  
		Last Modified: Mon, 25 Mar 2024 19:13:38 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ca1a63bc2d0b667b9f352812c41bff32a05ab075d43c91315bc8904500f1d2`  
		Last Modified: Mon, 25 Mar 2024 19:13:38 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c3839c5da6424358591d4dce122b39af2a923a548932f39c866f0b7417d6d0`  
		Last Modified: Mon, 25 Mar 2024 19:13:38 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8015ac97f73ef57e49b6ddd8db49af70f0d5053243f067e7fd14499c9fbadf`  
		Last Modified: Mon, 25 Mar 2024 19:13:48 GMT  
		Size: 197.5 MB (197547154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707ba728e6851bd46be3d420e92e7d295d6601e8db8f27adae72ec98906ee348`  
		Last Modified: Mon, 25 Mar 2024 19:13:38 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:23-ea-jdk` - windows version 10.0.17763.5576; amd64

```console
$ docker pull openjdk@sha256:ac0262dbdb43256501c84b54981f7d261256bcb2506f436b613a9134c9f8ab2b
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2323513797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e639f6a29cc723e263c394f3fc5ecb4bed212943b93cdb6902430bb2322fa3b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Mon, 25 Mar 2024 19:12:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Mar 2024 19:13:26 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 25 Mar 2024 19:13:27 GMT
ENV JAVA_HOME=C:\openjdk-23
# Mon, 25 Mar 2024 19:13:54 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 25 Mar 2024 19:13:54 GMT
ENV JAVA_VERSION=23-ea+15
# Mon, 25 Mar 2024 19:13:55 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/15/GPL/openjdk-23-ea+15_windows-x64_bin.zip
# Mon, 25 Mar 2024 19:13:55 GMT
ENV JAVA_SHA256=990a13730f096e195392211ecd4623c364cae742a9aedb5aae232c629b08f2b6
# Mon, 25 Mar 2024 19:15:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 25 Mar 2024 19:15:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ce779cbfb22f401e8d5c556f71e8c90160dfd5b2d1fafc6342ab1bd9af0317`  
		Last Modified: Mon, 25 Mar 2024 19:15:34 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f78e58f09f2cd12c4d3071c2aa5cea5ae564ac896cf164147de5a6ff90e533`  
		Last Modified: Mon, 25 Mar 2024 19:15:34 GMT  
		Size: 499.4 KB (499384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69458586865f6c2e6c06d233c24740903d4d06e564fdb4e633593866e3fd2be3`  
		Last Modified: Mon, 25 Mar 2024 19:15:34 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae832d578388a04ff6f307044f96dae9b6c0fbdc3d5e032eee9c64cc89c24b75`  
		Last Modified: Mon, 25 Mar 2024 19:15:33 GMT  
		Size: 350.8 KB (350831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fecd58f0c432ada491e7c8eb0ce0827c2a3fb7dd45d72a2f33dcb606a3376b5`  
		Last Modified: Mon, 25 Mar 2024 19:15:31 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:397ecb025be40a4180ec4f0b5abada2bfe2c1c2537170c5e60be68269885af92`  
		Last Modified: Mon, 25 Mar 2024 19:15:32 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b05333eec4b8574c88a845e9bb482c0af5f0dd9f357c039a3770d6b2ad57924`  
		Last Modified: Mon, 25 Mar 2024 19:15:32 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d75eac12b817d0758382e3e87f8282b87a768d2e15408a72add5cfc1f4d8d4`  
		Last Modified: Mon, 25 Mar 2024 19:15:44 GMT  
		Size: 197.6 MB (197555868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d919a774c212eaad50de52369b0ecf373cf927f89f9a62515520f62c9273d1f3`  
		Last Modified: Mon, 25 Mar 2024 19:15:32 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
