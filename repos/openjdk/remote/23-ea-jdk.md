## `openjdk:23-ea-jdk`

```console
$ docker pull openjdk@sha256:255d114348622812338826cc54a7c9a8a3ea20565b31d37c7a71af301764d920
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
$ docker pull openjdk@sha256:ffaa1e6de7495bbea0af45b24e569ad26db11f1cef608a2e7d1d382ba5d926f5
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2155860773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b945cfcb15ea0d01ec43d2883d28cd20d705794c982444b7c09b5ab8a2f6ca7`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Sat, 16 Mar 2024 00:02:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 16 Mar 2024 00:03:14 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 16 Mar 2024 00:03:15 GMT
ENV JAVA_HOME=C:\openjdk-23
# Sat, 16 Mar 2024 00:03:21 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 16 Mar 2024 00:03:22 GMT
ENV JAVA_VERSION=23-ea+14
# Sat, 16 Mar 2024 00:03:23 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/14/GPL/openjdk-23-ea+14_windows-x64_bin.zip
# Sat, 16 Mar 2024 00:03:24 GMT
ENV JAVA_SHA256=bda022a1843857170a5addfeffecf490af3c3b93a8925899193a09a093bd8b4b
# Sat, 16 Mar 2024 00:03:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 16 Mar 2024 00:03:47 GMT
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
	-	`sha256:5a4f5d3d1534dc31c2c30f1f0700d76a2359b2401c6291e7a39a5abac649d3be`  
		Last Modified: Sat, 16 Mar 2024 00:03:56 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9525845d439d75526f992868a56075c10cc3fb848b2c8eba33fff869b4bc5a8`  
		Last Modified: Sat, 16 Mar 2024 00:03:56 GMT  
		Size: 500.6 KB (500577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abfef0bbe213d3118837b6fc7d7894b2f0abfa97ac8fc78d7673a1d82410793b`  
		Last Modified: Sat, 16 Mar 2024 00:03:55 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6910c9de71018e135079124723424307ecfa26f13c28b67168da674be53516`  
		Last Modified: Sat, 16 Mar 2024 00:03:55 GMT  
		Size: 345.9 KB (345950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d89541af641c08a1a8628c51a58e38d1789444896e7c47a42c7cb176b043aa`  
		Last Modified: Sat, 16 Mar 2024 00:03:53 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e262ff571edbf09e77eef8e33e138948eb43aa0aae511d14f10f3a910f2ae4`  
		Last Modified: Sat, 16 Mar 2024 00:03:53 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a39e11aba6703bd269a0a633a00da1d03f44f365c7173a36de71677fc841adf`  
		Last Modified: Sat, 16 Mar 2024 00:03:53 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f26714a18e8b1a42e2d38096f45fbf75e1d0f76fe68c1948e36edae9256c98c4`  
		Last Modified: Sat, 16 Mar 2024 00:04:05 GMT  
		Size: 197.5 MB (197547477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89270f1447ed53cbcf0273a00dd0b9a0fd1d636ec1bd3b2cfca3b139c6e551c3`  
		Last Modified: Sat, 16 Mar 2024 00:03:53 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:23-ea-jdk` - windows version 10.0.17763.5576; amd64

```console
$ docker pull openjdk@sha256:6e41489b877186eec4356911042d7a09afc19ca2e66cc7174c4597549d2dc0db
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2323521672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:492017700287e379a7303a6ff5c3c0e8b6a0a531e41ec83d8b698c5d462393e9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Sat, 16 Mar 2024 00:09:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 16 Mar 2024 00:10:44 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 16 Mar 2024 00:10:45 GMT
ENV JAVA_HOME=C:\openjdk-23
# Sat, 16 Mar 2024 00:11:06 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 16 Mar 2024 00:11:06 GMT
ENV JAVA_VERSION=23-ea+14
# Sat, 16 Mar 2024 00:11:07 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/14/GPL/openjdk-23-ea+14_windows-x64_bin.zip
# Sat, 16 Mar 2024 00:11:07 GMT
ENV JAVA_SHA256=bda022a1843857170a5addfeffecf490af3c3b93a8925899193a09a093bd8b4b
# Sat, 16 Mar 2024 00:11:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 16 Mar 2024 00:11:46 GMT
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
	-	`sha256:04d2f68ae3e563c996f31cd13becfd8280e7e567b09b35afaa510442e0794846`  
		Last Modified: Sat, 16 Mar 2024 00:11:51 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8c9090aff08cac5ebf902591b1f6c6e354d89f7f91e659d0800d653842f2a7`  
		Last Modified: Sat, 16 Mar 2024 00:11:51 GMT  
		Size: 500.7 KB (500694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa70658817ea2b0dac2d1a97be4aebb9bea5cca601bd67fbb7b9d01703a3ccc`  
		Last Modified: Sat, 16 Mar 2024 00:11:50 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c16a365b8c0cb7c82ad301c930294b3b6835ed6e2d7fd4e129345f4cd4f94380`  
		Last Modified: Sat, 16 Mar 2024 00:11:50 GMT  
		Size: 351.4 KB (351443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ac9308262785d3bf45a6b8f57d5943fcb057d9b4dd8fc733fb23b824f37d3`  
		Last Modified: Sat, 16 Mar 2024 00:11:49 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50253595937ab0ff7ec41baf9f92295fbb575b8b134dff7a04e9acdbc27d2a09`  
		Last Modified: Sat, 16 Mar 2024 00:11:49 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014201f5c854e92ee3a5fed7e66168dabb0095fd5ff4e27b3a4504961b868f55`  
		Last Modified: Sat, 16 Mar 2024 00:11:49 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd33e958a3a7687ba829e566091a8d96b571e76df273bcdebd48908c160d5ff`  
		Last Modified: Sat, 16 Mar 2024 00:12:01 GMT  
		Size: 197.6 MB (197561758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14cb96c77054ab52868d42e1b5863192bc1a8e2866a49583c83614817745211a`  
		Last Modified: Sat, 16 Mar 2024 00:11:49 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
