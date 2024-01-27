## `openjdk:22-ea-jdk`

```console
$ docker pull openjdk@sha256:f208d162fe97da704eb87376fc0f5ac973a85ffe5efeb5ad8bea5006f251f23f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `openjdk:22-ea-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:31afa4a4438d970ee3c9d68cf82535a5a7c474bcd5706c0a1811a5ccfdec77ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.1 MB (269080138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70d691a10226d37819f4e9f3ee2f504eddbb6d40ca0f058312343316586b796c`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:45 GMT
ADD file:a1f24204c7f65fe2362a45e81d2d867cc73405d4bf548fd36ff720ee36fe25ef in / 
# Wed, 17 Jan 2024 21:34:46 GMT
CMD ["/bin/bash"]
# Tue, 23 Jan 2024 19:48:26 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 23 Jan 2024 19:48:26 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Tue, 23 Jan 2024 19:48:26 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jan 2024 19:48:26 GMT
ENV LANG=C.UTF-8
# Tue, 23 Jan 2024 19:48:26 GMT
ENV JAVA_VERSION=22-ea+32
# Tue, 23 Jan 2024 19:48:26 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/32/GPL/openjdk-22-ea+32_linux-x64_bin.tar.gz'; 			downloadSha256='7ac0b8815f22c852796fa13b7680e07fa1dc340aa93f5e2bf1c5502337d952d6'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/32/GPL/openjdk-22-ea+32_linux-aarch64_bin.tar.gz'; 			downloadSha256='7c565754b2926817c1779683d6b8f1975a94a8731fad35a670ea669a77aea182'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 23 Jan 2024 19:48:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:558b7d69a2e576e93c7cb18ecd087a92959e912b116323c188183d5cf8ab5b17`  
		Last Modified: Wed, 17 Jan 2024 21:36:52 GMT  
		Size: 51.3 MB (51321731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e67dfd05b0269f7296b15d6c3eae2c96f50d3f45e2df00d2fe7338ca7d320b`  
		Last Modified: Wed, 24 Jan 2024 20:50:28 GMT  
		Size: 15.0 MB (14990931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785d85712376f9db22b3fab3b324efe06d639c97c2f013e23a61a17a532b819d`  
		Last Modified: Wed, 24 Jan 2024 20:50:30 GMT  
		Size: 202.8 MB (202767476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:5f07b58887cf63ba6230334d5156d2ac2c5d42bf5bea2d873203e303d1cc0897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1935748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a4a96efcf5b42f40dddd167ee3a04b0a49491b787f439a8d3c93d474760fe5`

```dockerfile
```

-	Layers:
	-	`sha256:507ccdaa6cc660ef176c5b8aaff2587619bd1fa2ae7809b8e580b42f4e54300d`  
		Last Modified: Wed, 24 Jan 2024 20:50:27 GMT  
		Size: 1.9 MB (1915859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:935ad95554d1d6ace76c57e04f451f9a93e672f981d93e45a4a98cded9975302`  
		Last Modified: Wed, 24 Jan 2024 20:50:28 GMT  
		Size: 19.9 KB (19889 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-ea-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:66e50283bac3621207ca068690e27c075fa48cb7fe8c94e12f6c6858dbe9f484
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.6 MB (266596613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d50ed1a8257969c7d3966e80180ba8a28267b0eeeb3e17dd605cc3433c4a58`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 17 Jan 2024 22:07:51 GMT
ADD file:d9c5a5624a292383f8c072d816e66770afc4dfd0215037516136df1ced9a2994 in / 
# Wed, 17 Jan 2024 22:07:52 GMT
CMD ["/bin/bash"]
# Tue, 23 Jan 2024 19:48:26 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 23 Jan 2024 19:48:26 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Tue, 23 Jan 2024 19:48:26 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jan 2024 19:48:26 GMT
ENV LANG=C.UTF-8
# Tue, 23 Jan 2024 19:48:26 GMT
ENV JAVA_VERSION=22-ea+32
# Tue, 23 Jan 2024 19:48:26 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/32/GPL/openjdk-22-ea+32_linux-x64_bin.tar.gz'; 			downloadSha256='7ac0b8815f22c852796fa13b7680e07fa1dc340aa93f5e2bf1c5502337d952d6'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/32/GPL/openjdk-22-ea+32_linux-aarch64_bin.tar.gz'; 			downloadSha256='7c565754b2926817c1779683d6b8f1975a94a8731fad35a670ea669a77aea182'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 23 Jan 2024 19:48:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6988ac25ab22b91e9e2b9b71df8fcdc44661212c4214d47ad649398b4192a99e`  
		Last Modified: Wed, 17 Jan 2024 22:09:30 GMT  
		Size: 50.1 MB (50074578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbecf34c8e1a9b9949041e4c9e805d7ee8c1f00ad6362349a4579d6db495c27`  
		Last Modified: Thu, 18 Jan 2024 10:42:33 GMT  
		Size: 15.7 MB (15702213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a927ef34b5744c7368fdb38dac50523a2e553c7d55a20adbdc24aebfaa5db8c0`  
		Last Modified: Thu, 25 Jan 2024 04:30:26 GMT  
		Size: 200.8 MB (200819822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:50f7c4ba7a787c6e8dd4da39261906b64992fa3d6aba39ae1ffd5ef7ba2ddd89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1934193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7c01c359a49d0c20cf1ae6286e6d701ece6d7f40e12eec39f86f8efaf437e91`

```dockerfile
```

-	Layers:
	-	`sha256:621316240c68ed1d47aa16e0ddf3265e2b0cf25cb02704760425c0e69ae154d5`  
		Last Modified: Thu, 25 Jan 2024 04:30:18 GMT  
		Size: 1.9 MB (1914433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:843e92e832e5a388bdea34cc16b16a121f4f75ad7be89ac17d10a7171bd5e81d`  
		Last Modified: Thu, 25 Jan 2024 04:30:18 GMT  
		Size: 19.8 KB (19760 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-ea-jdk` - windows version 10.0.20348.2227; amd64

```console
$ docker pull openjdk@sha256:c6f625e00eb17d3edf050daaacc8683c146d140f37ce2493fba1007ec217ecbb
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2098745551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5784922378d0275f76c56d9f333ac3ac638a46520622091ff6921a9a827311`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Fri, 26 Jan 2024 23:49:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 26 Jan 2024 23:50:53 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 26 Jan 2024 23:50:54 GMT
ENV JAVA_HOME=C:\openjdk-22
# Fri, 26 Jan 2024 23:51:01 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 26 Jan 2024 23:51:02 GMT
ENV JAVA_VERSION=22-ea+33
# Fri, 26 Jan 2024 23:51:03 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/33/GPL/openjdk-22-ea+33_windows-x64_bin.zip
# Fri, 26 Jan 2024 23:51:03 GMT
ENV JAVA_SHA256=7314e1a93eac080af82b5a8e301d653e3e4878f3fc01d6e41559cacf8ad8ab2b
# Fri, 26 Jan 2024 23:52:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 26 Jan 2024 23:52:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9210ce567aecdf96d975b23f490eee629d5a936195f7bc9fff853ab4c6b4d86`  
		Last Modified: Fri, 26 Jan 2024 23:52:25 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2857cba891600d502f76fc7c9a00beed1c4827d348d9d95d19e56a0af79c558`  
		Last Modified: Fri, 26 Jan 2024 23:52:25 GMT  
		Size: 496.2 KB (496186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d50622e67319403538740012196899b678a08a2b437e214a5cb53f0223db262`  
		Last Modified: Fri, 26 Jan 2024 23:52:25 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c3ec7b391598e5d2d38196ffae658187a07b37b2ae966e8b9cca91cd2ca9ccb`  
		Last Modified: Fri, 26 Jan 2024 23:52:25 GMT  
		Size: 313.9 KB (313873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e485789ba022b613c06f337795427bda4275b78cbc76973bc5b1cb37fa38baa`  
		Last Modified: Fri, 26 Jan 2024 23:52:24 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cc4bb5505bfdbf4a60ad13049cd474c1c963f14bbd27348a31ba5a22d6229f`  
		Last Modified: Fri, 26 Jan 2024 23:52:24 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45968ad5848795f27af9da704747ddc0aedd56675958601c84792f66225ae02e`  
		Last Modified: Fri, 26 Jan 2024 23:52:24 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46408d157bb9bfcd0ad0586b648076f7829de09a662b3b0c13a7426ff62de382`  
		Last Modified: Fri, 26 Jan 2024 23:52:34 GMT  
		Size: 197.7 MB (197715017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e587e56cae671fc0e2afca3b7e9f00de69d01cf217f4b76a7d7f9c17599fb0dd`  
		Last Modified: Fri, 26 Jan 2024 23:52:24 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-jdk` - windows version 10.0.17763.5329; amd64

```console
$ docker pull openjdk@sha256:956010d9e2bb9237e52fcf2016bae33287a6e37cb0e222984b6aa81c6a99fcb6
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2268388053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b43d179e1e8e589c749e2ebf9ac8be413abd88a12113a2e74d8cdc2282615a6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Fri, 26 Jan 2024 23:49:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 26 Jan 2024 23:51:44 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 26 Jan 2024 23:51:44 GMT
ENV JAVA_HOME=C:\openjdk-22
# Fri, 26 Jan 2024 23:52:08 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 26 Jan 2024 23:52:08 GMT
ENV JAVA_VERSION=22-ea+33
# Fri, 26 Jan 2024 23:52:09 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/33/GPL/openjdk-22-ea+33_windows-x64_bin.zip
# Fri, 26 Jan 2024 23:52:09 GMT
ENV JAVA_SHA256=7314e1a93eac080af82b5a8e301d653e3e4878f3fc01d6e41559cacf8ad8ab2b
# Fri, 26 Jan 2024 23:52:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 26 Jan 2024 23:52:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f13d0db08ff1cf3d1cf5e5d69c38c08e93e4a16ee04f73fff59b494f5371b91e`  
		Last Modified: Fri, 26 Jan 2024 23:52:58 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:337e49d253acb8d77744592c88dfd744fe84d6e997d29e5349d131a4396263f4`  
		Last Modified: Fri, 26 Jan 2024 23:52:58 GMT  
		Size: 517.9 KB (517942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77be480b51413878c573ebc55ed9099eda30decb74eddababcb99c12bcacb735`  
		Last Modified: Fri, 26 Jan 2024 23:52:57 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef18ea67753a1ddf3dcaa36d4e9c79124eb4745d47dd53dc6969e1887a86207b`  
		Last Modified: Fri, 26 Jan 2024 23:52:57 GMT  
		Size: 363.7 KB (363672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707092397b71edb630eb2ef4f7a7f21e30f09e996395609806d06440655b674d`  
		Last Modified: Fri, 26 Jan 2024 23:52:56 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca173c88c111c2c06e91fa1a5e20079821f006bcc5f6cec1976070c8b83ff45b`  
		Last Modified: Fri, 26 Jan 2024 23:52:56 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a78fe5e68dfe3d677c6318049a30c8306fd52c80b1ad6c19a1cc005a6263607`  
		Last Modified: Fri, 26 Jan 2024 23:52:56 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a3a4d99f65185dd2fbdb945c050ce51bd215298dfd18a15de3602cfc4d85b2`  
		Last Modified: Fri, 26 Jan 2024 23:53:06 GMT  
		Size: 197.8 MB (197776178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b6bb5c5ef5bfc2188915fd6c3d74d4b743e5acc4629585bbd54812a2dd4c681`  
		Last Modified: Fri, 26 Jan 2024 23:52:56 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
