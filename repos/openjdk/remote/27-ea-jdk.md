## `openjdk:27-ea-jdk`

```console
$ docker pull openjdk@sha256:b1f05c7c572c41f797ab528ce9c17d144f3e5191f2bf739859c356022edf03db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.32995; amd64
	-	windows version 10.0.20348.5256; amd64

### `openjdk:27-ea-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:fa8f624eef77f67158b3c8c8f886509ca35afc5f3252c8967172d2f70517d19f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.7 MB (307715672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ce02b6562ef13642347a98c1f9d7a879dd8c44cb1c47ab8dafe3eac3128e6f5`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:44:08 GMT
ADD oraclelinux-10-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:08 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 22:37:23 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 22 Jun 2026 22:37:33 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 22 Jun 2026 22:37:33 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:37:33 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 22:37:33 GMT
ENV JAVA_VERSION=27-ea+27
# Mon, 22 Jun 2026 22:37:33 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/27/GPL/openjdk-27-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='4f81468b39b9f6516ce5e3de3130e404d508be7d77d601ec1217056163ff6a6e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/27/GPL/openjdk-27-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='048e4f60c3069ab86e0a068eedd93e33e62ec275a1b2a9033bb07c925f01b7c9'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 22 Jun 2026 22:37:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ded2aa0abafd1e1e93e05338cb1b14916dbeb283d3862aa21e5d8b0164f4cbf3`  
		Last Modified: Tue, 12 May 2026 18:44:20 GMT  
		Size: 43.1 MB (43080582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67891505540a6bb44e488b874e37e31e860e46cfe6e0fe2cdf5c64cd3a8c9ece`  
		Last Modified: Mon, 22 Jun 2026 22:37:57 GMT  
		Size: 37.7 MB (37687115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcefd717c7552e4909ff47db61dff7cba2ea07e955948f8d518794e03bf52a5b`  
		Last Modified: Mon, 22 Jun 2026 22:38:00 GMT  
		Size: 226.9 MB (226947975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:022657bf1c47e39f3a899ccf518bcc72b76096a101e16cfaad845f552d16ff6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57893277910a7a6e17ce58596f83eadf677ca3bc2a4abc8f715b1a518efce4f5`

```dockerfile
```

-	Layers:
	-	`sha256:e7dc1287f26d07f049c4092a0ff55f6885d23aa1671de605dc8335b0b6db19f8`  
		Last Modified: Mon, 22 Jun 2026 22:37:55 GMT  
		Size: 2.4 MB (2366462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddca57e6200add1088dd7a983e3399f35dc69320a62bd21d9f8e3a001dd2b4c1`  
		Last Modified: Mon, 22 Jun 2026 22:37:55 GMT  
		Size: 17.8 KB (17849 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:da794d72b97accba444a5148417af945f38f7917b99205c6c41d99dd072db2c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304126100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a807a53e1e8a9c60ad1c4516c32306eab2e9b4b12b3baf0e0c4ca0212ee49690`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:43:55 GMT
ADD oraclelinux-10-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:43:55 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 22:37:06 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 22 Jun 2026 22:37:17 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 22 Jun 2026 22:37:17 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:37:17 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 22:37:17 GMT
ENV JAVA_VERSION=27-ea+27
# Mon, 22 Jun 2026 22:37:17 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/27/GPL/openjdk-27-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='4f81468b39b9f6516ce5e3de3130e404d508be7d77d601ec1217056163ff6a6e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/27/GPL/openjdk-27-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='048e4f60c3069ab86e0a068eedd93e33e62ec275a1b2a9033bb07c925f01b7c9'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 22 Jun 2026 22:37:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:523b5fcd95921b1880258a8c56e30985e8f3adf21d143bf177907dc76d6a562b`  
		Last Modified: Tue, 12 May 2026 18:44:06 GMT  
		Size: 41.5 MB (41495695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7794d6854b519666fc859dd76426bc35de4170b704c06948c2017fe6d9b6fb04`  
		Last Modified: Mon, 22 Jun 2026 22:37:41 GMT  
		Size: 37.7 MB (37696104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5a4ff07b62e314045fab799dcbf40f7d87769dd158659a50abf141b55e1acc`  
		Last Modified: Mon, 22 Jun 2026 22:37:45 GMT  
		Size: 224.9 MB (224934301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:5eba6d83b3b986518a1e0a8afa7f8a24bff220d389103b083672a6946183e1ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842d100eb579b442dce7274124e95b2ac820e24cf8a1c1281b2ba559af1d27de`

```dockerfile
```

-	Layers:
	-	`sha256:924bf57963087f9d71c22cb2916286c5055742da82435b48a13804ccfb006ef6`  
		Last Modified: Mon, 22 Jun 2026 22:37:40 GMT  
		Size: 2.4 MB (2365990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2d3f453622a0fcb2567532659b77fe26fd49f0f7ebfb0dd9ac67aa07f679832`  
		Last Modified: Mon, 22 Jun 2026 22:37:40 GMT  
		Size: 18.1 KB (18065 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk` - windows version 10.0.26100.32995; amd64

```console
$ docker pull openjdk@sha256:45977a26545a29827dce031dc4558116165ea1301f6625da1004a5616841555c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2503478433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de4255d17527c24f1bcf6ed3372a6f5a45a370f559f9cb2bd796c7a734313493`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Mon, 22 Jun 2026 22:44:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 22 Jun 2026 22:46:00 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 22 Jun 2026 22:46:00 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 22 Jun 2026 22:46:07 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 22 Jun 2026 22:46:08 GMT
ENV JAVA_VERSION=27-ea+27
# Mon, 22 Jun 2026 22:46:08 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/27/GPL/openjdk-27-ea+27_windows-x64_bin.zip
# Mon, 22 Jun 2026 22:46:09 GMT
ENV JAVA_SHA256=95f2039dcf26a1c012aaa98a839b7c4ccc5974f9697e6d7c7c6a332afcf12fed
# Mon, 22 Jun 2026 22:46:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 22 Jun 2026 22:46:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee71d57b2226db82d002abc39a97b7dd144f007db435566364a0285bf115b83`  
		Last Modified: Tue, 09 Jun 2026 18:08:12 GMT  
		Size: 756.1 MB (756083682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8323c80a7f544f650118cc07ff573d79bad528c94c6994476943c1271d2034dc`  
		Last Modified: Mon, 22 Jun 2026 22:46:48 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7989b1f39645f7cd91f59249046be9d11f03fb07c9d5b80536e11fa92b277491`  
		Last Modified: Mon, 22 Jun 2026 22:46:48 GMT  
		Size: 407.5 KB (407468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3438329670602264a5199cbb1f0f59ebd0ea2e0049db69feaa625544d6b8e07c`  
		Last Modified: Mon, 22 Jun 2026 22:46:48 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4264cc044190a364f24d7c456b64463f73c511c93c435d3db64b2841d1d87af1`  
		Last Modified: Mon, 22 Jun 2026 22:46:48 GMT  
		Size: 396.2 KB (396227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14dfe1bd813aa820de4fe9c0833a7859ccd6e348c2d626a4e55cd97e00dcba17`  
		Last Modified: Mon, 22 Jun 2026 22:46:46 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf8205d8e3476e38c1d17952dd9443012cab97be6f337d69e3b81f8e38fbd2a9`  
		Last Modified: Mon, 22 Jun 2026 22:46:46 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e7cc44e40eaa03fadb796a5c65af5960f5a52e14fd0c017a7becd085c9f036`  
		Last Modified: Mon, 22 Jun 2026 22:46:46 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9bf9e65e6701b000df86b196168ff3135c3b5c1e649da72f33e3db18cefbb0a`  
		Last Modified: Mon, 22 Jun 2026 22:47:02 GMT  
		Size: 223.5 MB (223523980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8bd05d57f03696d008da55bb6127c5157ac28bddf478a82ff84ea7677d1aea9`  
		Last Modified: Mon, 22 Jun 2026 22:46:46 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-jdk` - windows version 10.0.20348.5256; amd64

```console
$ docker pull openjdk@sha256:e048a4ca63828a80c91e1d4243d37bcd084817a075227ca98b54372bdd2c4aff
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2356493763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a88bc863c516de819abdb42c530d594dd1151391e93c730cd69d990eff6cdd54`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Mon, 22 Jun 2026 22:44:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 22 Jun 2026 22:45:16 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 22 Jun 2026 22:45:17 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 22 Jun 2026 22:45:26 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 22 Jun 2026 22:45:27 GMT
ENV JAVA_VERSION=27-ea+27
# Mon, 22 Jun 2026 22:45:27 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/27/GPL/openjdk-27-ea+27_windows-x64_bin.zip
# Mon, 22 Jun 2026 22:45:29 GMT
ENV JAVA_SHA256=95f2039dcf26a1c012aaa98a839b7c4ccc5974f9697e6d7c7c6a332afcf12fed
# Mon, 22 Jun 2026 22:46:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 22 Jun 2026 22:46:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c95a3509eb5b1e3191c0c24f4e8d70327752ac2b10ac257f83ad7555d263ee1`  
		Last Modified: Mon, 22 Jun 2026 22:46:49 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c346f0d4d92e655eb3a2ada75422b42a066d7817184a8b161363b8cf4f437750`  
		Last Modified: Mon, 22 Jun 2026 22:46:50 GMT  
		Size: 502.4 KB (502416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad18c4c77cb604f9aed745b28124908916593ba55de3defd3d416b9ed5e60cb`  
		Last Modified: Mon, 22 Jun 2026 22:46:49 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9b221005e200979d08b3d8ef1cd1359f6d49de2db1ad2419d4d5b198f8d42b3`  
		Last Modified: Mon, 22 Jun 2026 22:46:49 GMT  
		Size: 352.2 KB (352208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1248870a9b37975620492cc95b831602f8340587f9d8ff0b95cbc2f908547d`  
		Last Modified: Mon, 22 Jun 2026 22:46:47 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06cfbb859d3cdbc93be9ed335a20ad4436647dd7d80f80cdf545f96f3a2f7052`  
		Last Modified: Mon, 22 Jun 2026 22:46:47 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d158d53a993eb382bf1f611bc359f77a733ab166e9cebc8fca7f6ec8c484a8e9`  
		Last Modified: Mon, 22 Jun 2026 22:46:48 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c92dadbba67903e0eb8376fc8b7ccc1dca8dd09d684d41f0b23e05c7302b793`  
		Last Modified: Mon, 22 Jun 2026 22:47:02 GMT  
		Size: 223.5 MB (223505748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a894cdac940df41f38ad86a46384b8f84dc6ab593cdd7da5802a0108eaded6e`  
		Last Modified: Mon, 22 Jun 2026 22:46:47 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
