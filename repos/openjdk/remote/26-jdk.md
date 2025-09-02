## `openjdk:26-jdk`

```console
$ docker pull openjdk@sha256:f6a9bb937cc656e5458c088b60436e08eb142ea4c60307fd820bfab299cdc203
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `openjdk:26-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:c85d7e4a9c17b09da7511d646505050dc7211eb40fbf5bfd974c99ba3d2dc546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.7 MB (310683121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca8eae1dfbd576738a6976c25494eeca29382947b16b7ff42adbdcdbae2f5f4b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Sat, 30 Aug 2025 00:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 30 Aug 2025 00:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 30 Aug 2025 00:48:13 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Aug 2025 00:48:13 GMT
ENV LANG=C.UTF-8
# Sat, 30 Aug 2025 00:48:13 GMT
ENV JAVA_VERSION=26-ea+13
# Sat, 30 Aug 2025 00:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/13/GPL/openjdk-26-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='bf1fc270d7d30fdafbb1df8cb75b7b9a0e40adba8b72e9655410df7d7475ecc0'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/13/GPL/openjdk-26-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='e0d0ccf09df66d71738ff9ba2a927e4169f52d99569f57a346797b83e2dea920'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 30 Aug 2025 00:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6bfa726944bdde2d3a824591b1bb2c176e79afac3179bc99fb5c0b0f7596c0`  
		Last Modified: Tue, 02 Sep 2025 17:24:43 GMT  
		Size: 38.0 MB (38004417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09033ad10c922f74b3a0005af640ef20c3d3bbc3607b629f53dd4e9ea1814a3`  
		Last Modified: Tue, 02 Sep 2025 18:28:49 GMT  
		Size: 223.2 MB (223181688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:6f8c513d47f7f868fb13965fd823524c55849f63b3240dd9e4dddcf9cadc07db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3660474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f849dba6b1544747ac29b9c55316770b1c57794773832db3e342405e0d8fe3`

```dockerfile
```

-	Layers:
	-	`sha256:a77a6ec374b005c2e72bc8071feec8e940d55e611ae4082b4a8593bc913e6b07`  
		Last Modified: Tue, 02 Sep 2025 18:23:53 GMT  
		Size: 3.6 MB (3640729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3004d71fba1f6f30a8fa933d9b4abc3d0a097ed0fd45a496a0217d8980b1b025`  
		Last Modified: Tue, 02 Sep 2025 18:23:54 GMT  
		Size: 19.7 KB (19745 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:9ff89798e17ae589cdf81d22712b00f970f9cd03f37fbc22a1af0aaef32128d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.5 MB (307465032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538c56065c43974c68d24c27f94b65c90017bce006c6bbf486743b3b324ee271`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Aug 2025 17:12:13 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:12:13 GMT
CMD ["/bin/bash"]
# Sat, 23 Aug 2025 00:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 23 Aug 2025 00:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 23 Aug 2025 00:48:14 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Aug 2025 00:48:14 GMT
ENV LANG=C.UTF-8
# Sat, 23 Aug 2025 00:48:14 GMT
ENV JAVA_VERSION=26-ea+12
# Sat, 23 Aug 2025 00:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/12/GPL/openjdk-26-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='2d6177e017ca138d8990643910b989990751db9370cd78dfc51e5116411e7f6f'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/12/GPL/openjdk-26-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='b4e0c4bb252fe005ad3a46c54264e226c554fe95edcbdc9df81dbc268901c7cb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 23 Aug 2025 00:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b5e369658cc0fdedce73e0479a85cd17ba8a09435fc3b21f6afb7e0d4783429d`  
		Last Modified: Thu, 21 Aug 2025 18:56:13 GMT  
		Size: 48.1 MB (48086723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f251bedb6d0a7854cec601a06650a41a8800628c25948fd9b15b8018354d6f6`  
		Last Modified: Thu, 21 Aug 2025 20:15:43 GMT  
		Size: 38.4 MB (38406411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae9fd6628c76e574a204d4d6720a32dd59a95911c00ef7249d109f36af8c062`  
		Last Modified: Tue, 26 Aug 2025 09:07:35 GMT  
		Size: 221.0 MB (220971898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:5344b9da1e0461546a1dd83e3177fa6167eb4b770fd068395bad3dc0afaf3637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3658524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3ff9082c795d3ccd633103d76c2ce27d975266391e868903db7feba6094ea8`

```dockerfile
```

-	Layers:
	-	`sha256:58299953a37202d113285c2c1e19e7289beee1ab1b547f418681bb6b7eadd842`  
		Last Modified: Tue, 26 Aug 2025 00:23:52 GMT  
		Size: 3.6 MB (3638491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e8ef1aaf55c85b7782df316f1a754c9690827cf56ae071947f8d0b831fbfbbe`  
		Last Modified: Tue, 26 Aug 2025 00:23:53 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-jdk` - windows version 10.0.26100.4946; amd64

```console
$ docker pull openjdk@sha256:4c69acb82a9c3bf74f16685c801f7b408efd30cedfa47cea45ec70d31d9db78c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3718708597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcce7d463302c4a64e9c6490430f010b79c3820c8225e14371c37d3aa250c94d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Tue, 02 Sep 2025 17:29:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Sep 2025 17:29:29 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 02 Sep 2025 17:29:30 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 02 Sep 2025 17:29:38 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 02 Sep 2025 17:29:39 GMT
ENV JAVA_VERSION=26-ea+13
# Tue, 02 Sep 2025 17:29:40 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/13/GPL/openjdk-26-ea+13_windows-x64_bin.zip
# Tue, 02 Sep 2025 17:29:41 GMT
ENV JAVA_SHA256=252a76f58ab825b56d6a57267338a4252c29c400ef3bdb956c94d2fb9bb183b6
# Tue, 02 Sep 2025 17:30:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 02 Sep 2025 17:30:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffcb282db45a8dce176e31162ff60ffc535abda80dc9980b60125235cbc0d7e2`  
		Last Modified: Tue, 02 Sep 2025 17:33:53 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ae95d00610c6ea73ba4873e0f3aa905e0983841c515126adefeb6a38071c3e`  
		Last Modified: Tue, 02 Sep 2025 17:33:53 GMT  
		Size: 377.5 KB (377496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6113c5175cd444916863656487724358e926ce43ad42ba0d42616c14746521`  
		Last Modified: Tue, 02 Sep 2025 17:33:53 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a049d80c1bbe79c5cca0a3ded06fdcb1b06fc0f6028e8cee947e6389c622723`  
		Last Modified: Tue, 02 Sep 2025 17:33:53 GMT  
		Size: 359.2 KB (359163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0095dbfed8063714c6dcbdf41a9bf311ad81f8df8e37f4a167ff4c2a30af568`  
		Last Modified: Tue, 02 Sep 2025 17:33:45 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a8423e122204ea192834989014a869adafca211693ba423fb8690596b863233`  
		Last Modified: Tue, 02 Sep 2025 17:33:45 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d62ae46b91ce44809f16176a5ffb43064613a534ab972943cadf0791390145`  
		Last Modified: Tue, 02 Sep 2025 17:33:45 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c97923f24f6cb850492bd21529a3773fedbbfa900a301fb81520b0520fa8c80e`  
		Last Modified: Tue, 02 Sep 2025 18:03:49 GMT  
		Size: 219.1 MB (219133373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741bc894abe7ab81038d7c06deb39155cecc89bde464aefdcc4fe62c06f5b5d0`  
		Last Modified: Tue, 02 Sep 2025 17:33:45 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-jdk` - windows version 10.0.20348.4052; amd64

```console
$ docker pull openjdk@sha256:331e1708a1c292177e598b418af5f43ead645eaeaac30abb853579a960397e45
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2501529862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd3ebb551bda4572fe7e51bd9d50829b1e33c208a6b64f34385a0c2eb834b313`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 02 Sep 2025 17:22:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Sep 2025 17:23:11 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 02 Sep 2025 17:23:12 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 02 Sep 2025 17:23:21 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 02 Sep 2025 17:23:22 GMT
ENV JAVA_VERSION=26-ea+13
# Tue, 02 Sep 2025 17:23:23 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/13/GPL/openjdk-26-ea+13_windows-x64_bin.zip
# Tue, 02 Sep 2025 17:23:24 GMT
ENV JAVA_SHA256=252a76f58ab825b56d6a57267338a4252c29c400ef3bdb956c94d2fb9bb183b6
# Tue, 02 Sep 2025 17:23:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 02 Sep 2025 17:23:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ded869c2c376350fbba0b5539f3f4027ed15425226ab107d3acac6c9f598e7e`  
		Last Modified: Tue, 02 Sep 2025 17:24:28 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e248cc3d62afcde60a6ebe57a0e116c0628710c5adba2611305420895ec3c4`  
		Last Modified: Tue, 02 Sep 2025 17:24:29 GMT  
		Size: 359.4 KB (359352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2754bc355d7737c6db4c55a1f9d730eaaf041cd02afd989b1087861abc8c8b7`  
		Last Modified: Tue, 02 Sep 2025 17:24:30 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286a8c40f74f5400809402ce1e70071a35d932c9f5a96a366954fcea19e4e303`  
		Last Modified: Tue, 02 Sep 2025 17:24:31 GMT  
		Size: 346.9 KB (346888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b74f4124d31eca69c1e081da68b8e0220defbf87cea0a8feb1d847caa362a7ff`  
		Last Modified: Tue, 02 Sep 2025 17:24:32 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d8e7b48cd39089f5e6f107bbd9348d60e427d9e48884cda41e07e11c88a70c`  
		Last Modified: Tue, 02 Sep 2025 17:24:33 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bc340254a8722788652f1594b8c532584a2055c8d66a7f1e145d75618777d22`  
		Last Modified: Tue, 02 Sep 2025 17:24:35 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436858895e6d1bb2d865e562d8716a8aa6cdfa1845de4d1a6cd094971c6ed04f`  
		Last Modified: Tue, 02 Sep 2025 18:03:05 GMT  
		Size: 219.1 MB (219123958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d87e249f2fa45909630a1657c07cc8fd0a22913bc62782e7f240e09d8bc418e5`  
		Last Modified: Tue, 02 Sep 2025 17:24:37 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
